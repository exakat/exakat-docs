.. _classes-usethis:

.. _use-this:

Use This
++++++++

.. meta::
	:description:
		Use This: Those methods should be using $this, or a static method or property.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use This
	:twitter:description: Use This: Those methods should be using $this, or a static method or property
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use This
	:og:type: article
	:og:description: Those methods should be using $this, or a static method or property
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/UseThis.html
	:og:locale: en
Those methods should be using `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_, or a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method or property.

A method that doesn't use any local data may be considered for a move : may be it doesn't belong here. 

The following functioncalls have been added, as access to the current class, without using `$this` or `self` : 

+ `get_class() <https://www.php.net/get_class>`_
+ `get_called_class() <https://www.php.net/get_called_class>`_
+ `get_object_vars() <https://www.php.net/get_object_vars>`_
+ `get_parent_class() <https://www.php.net/get_parent_class>`_
+ `get_class_vars() <https://www.php.net/get_class_vars>`_
+ `get_class_methods() <https://www.php.net/get_class_methods>`_

.. code-block:: php
   
   <?php
   
   class dog {
       private $name = 'Rex';
       
       // This method is related to the current object and class
       public function attaboy() {
           return Fetch, $this->name, Fetch\n;
       }
   
       // Not using any class related data : Does this belong here?
       public function addition($a, $b) {
           return $a + $b;
       }
   }
   ?>

See also `The Basics <https://www.php.net/manual/en/language.oop5.basic.php>`_.

Connex PHP features
-------------------

  + `$this <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24this.ini.html>`_
  + `self <https://php-dictionary.readthedocs.io/en/latest/dictionary/self.ini.html>`_
  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Suggestions
___________

* Add any use of $this pseudo-variable
* Move the method to another class
* Refactor the method as a function




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UseThis                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


