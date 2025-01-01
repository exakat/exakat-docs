.. _classes-unfinishedobject:

.. _unfinished-object:

Unfinished Object
+++++++++++++++++

.. meta::
	:description:
		Unfinished Object: Some of the properties are not assigned a value before or at constructor time.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unfinished Object
	:twitter:description: Unfinished Object: Some of the properties are not assigned a value before or at constructor time
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unfinished Object
	:og:type: article
	:og:description: Some of the properties are not assigned a value before or at constructor time
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/UnfinishedObject.html
	:og:locale: en
Some of the properties are not assigned a value before or at constructor time. Then, they might be called when one of the other public method is called, and yield a fatal `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   class x {
       private $p;
       private $p2;
       
       function __construct($p) {
           $this->p = $p;
           // $p2 is not assigned
       }
       
       function foo() {
           $this->p->goo();
           // This is not valid
           $this->p2->goo();
       }
   } 
   
   ?>

See also `Compulsory parameters should be required in your constructor <http://bestpractices.thecodingmachine.com/php/design_beautiful_classes_and_methods.html#compulsory-parameters-should-be-required-in-your-constructor>`_.

Connex PHP features
-------------------

  + `object <https://php-dictionary.readthedocs.io/en/latest/dictionary/object.ini.html>`_
  + `constructor <https://php-dictionary.readthedocs.io/en/latest/dictionary/constructor.ini.html>`_


Suggestions
___________

* Make sure the object is finished at construction time




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnfinishedObject                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.6                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


