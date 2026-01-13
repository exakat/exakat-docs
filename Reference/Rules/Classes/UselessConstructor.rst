.. _classes-uselessconstructor:

.. _useless-constructor:

Useless Constructor
+++++++++++++++++++

  Class constructor that have empty bodies are useless. They may be removed, as they are not called.

One edge case is when the class has a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, and the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ constructor must not be called.

Another edge case is promoted properties: the body of the constructor is still empty, but the parameters hold the definitions of properties. These might be better outside the constructor though.


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
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Cannot+call+constructor.html>`_



Connex PHP features
-------------------

  + `constructor <https://php-dictionary.readthedocs.io/en/latest/dictionary/constructor.ini.html>`_


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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


