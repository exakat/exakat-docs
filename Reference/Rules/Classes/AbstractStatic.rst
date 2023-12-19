.. _classes-abstractstatic:

.. _abstract-static-methods:

Abstract Static Methods
+++++++++++++++++++++++

  Methods cannot be both abstract and `static <https://www.php.net/manual/en/language.oop5.static.php>`_. `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods belong to a class, and will not be overridden by the child class. For normal methods, PHP will start at the object level, then go up the hierarchy to find the method. With `static <https://www.php.net/manual/en/language.oop5.static.php>`_, it is necessary to mention the name, or use Late `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ Binding, with `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ or `static <https://www.php.net/manual/en/language.oop5.static.php>`_. Hence, it is useless to have an abstract `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method : it should be a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method.

A child class is able to declare a method with the same name than a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method in the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, but those two methods will stay independent. 

This is not the case anymore in PHP 7.0+.


.. code-block:: php
   
   <?php
   
   abstract class foo {
       // This is not possible
       static abstract function bar() ;
   }
   
   ?>

See also `Why does PHP 5.2+ disallow abstract static class methods? <https://stackoverflow.com/questions/999066/why-does-php-5-2-disallow-abstract-static-class-methods>`_.


Suggestions
___________

* Remove abstract keyword from the method
* Remove static keyword from the method
* Remove the method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/AbstractStatic                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | method, abstract, constant                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


