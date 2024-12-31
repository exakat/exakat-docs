.. _classes-propertyusedinonemethodonly:

.. _property-used-in-one-method-only:

Property Used In One Method Only
++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Property Used In One Method Only: Properties should be used in several methods.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Property Used In One Method Only
	:twitter:description: Property Used In One Method Only: Properties should be used in several methods
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Property Used In One Method Only
	:og:type: article
	:og:description: Properties should be used in several methods
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/PropertyUsedInOneMethodOnly.html
	:og:locale: en
  Properties should be used in several methods. When a property is used in only one method, this should have be of another shape. 

Properties used in one method only may be used several times, and read only. This may be a class constant. Such properties are meant to be overwritten by an extending class, and that's possible with class constants.

Properties that read and written may be converted into a variable, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ to the method. This way, they are kept close to the method, and do not pollute the object's properties.
This analysis consider that using the current object with a cast or with the `get_object_vars() <https://www.php.net/get_object_vars>`_ function is also a usage, and skip those properties.

Note : properties used only once are not returned by this analysis. They are omitted, and are available in the analysis `Used Once Property`_.

.. code-block:: php
   
   <?php
   
   class foo {
       private $once = 1;
       const ONCE = 1;
       private $counter = 0;
       
       function bar() {
           // $this->once is never used anywhere else. 
           someFunction($this->once);
           someFunction(self::ONCE);   // Make clear that it is a 
       }
   
       function bar2() {
           static $localCounter = 0;
           $this->counter++;
           
           // $this->once is only used here, for distinguising calls to someFunction2
           if ($this->counter > 10) { // $this->counter is used only in bar2, but it may be used several times
               return false;
           }
           someFunction2($this->counter);
   
           // $localCounter keeps track for all the calls
           if ($localCounter > 10) { 
               return false;
           }
           someFunction2($localCounter);
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Suggestions
___________

* Drop the property, and inline the value
* Drop the property, and make the property a local variable
* Use the property in another method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PropertyUsedInOneMethodOnly                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.3                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-contao-classes-propertyusedinonemethodonly`                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


