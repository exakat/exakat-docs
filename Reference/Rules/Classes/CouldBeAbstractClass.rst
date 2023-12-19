.. _classes-couldbeabstractclass:

.. _could-be-abstract-class:

Could Be Abstract Class
+++++++++++++++++++++++

  An abstract class is never instantiated, and has children class that are. As such, a '`parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_' class that is never instantiated by itself, but has its own children instantiated could be marked as abstract. 

That will prevent new code to try to instantiate it.


.. code-block:: php
   
   <?php
   
   // Example code would actually be split over multiple files.
   
   
   // That class could be abstract
   class motherClass {}
   
   // Those classes shouldn't be abstract
   class firstChildren extends motherClass {}
   class secondChildren extends motherClass {}
   class thirdChildren extends motherClass {}
   
   new firstChildren();
   new secondChildren();
   new thirdChildren();
   
   //Not a single : new motherClass()
   
   ?>

See also `Class Abstraction <https://www.php.net/abstract>`_ and `Abstract classes and methods <https://phpenthusiast.com/object-oriented-php-tutorials/abstract-classes-and-methods>`_.


Suggestions
___________

* Make this class an abstract class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeAbstractClass                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | abstract                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-edusoho-classes-couldbeabstractclass`, :ref:`case-shopware-classes-couldbeabstractclass`                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


