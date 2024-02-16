.. _classes-uselessconstructor:

.. _useless-constructor:

Useless Constructor
+++++++++++++++++++

  Class constructor that have empty bodies are useless. They may be removed, as they are not called.

The only edge case is when the class has a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, and that constructor should not be called.


.. code-block:: php
   
   <?php
   
   class X {
       function __construct() {
           // Do nothing
       }
   }
   
   class Y extends X {
       // Useful constructor, as it prevents usage of the parent
       function __construct() {
           // Do nothing
       }
   }
   
   ?>

Suggestions
___________

* Remove the constructor




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UselessConstructor                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
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
| Features     | constructor                                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


