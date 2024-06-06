.. _structures-declarestaticonce:

.. _declare-static-once:

Declare Static Once
+++++++++++++++++++

  Global and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables should be declared only once in a method. It is also recommended to configure it at the beginning of the method. This could be refined by defining the variable at the last common moment, though it lacks readability.
Defining `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or global methods late is a micro-optimisation.

.. code-block:: php
   
   <?php
   
   function foo() {
       if (rand(0, 1)) {
           static $x;
           
           ++$x;
       } else {
           static $x;
           
           --$x;
       }
   }
   
   ?>

Suggestions
___________

* Remove duplicate static and global calls
* Move the static and global calls to the beginning of the method
* Refactor the static and global variable to properties




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DeclareStaticOnce                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.3 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | static                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


