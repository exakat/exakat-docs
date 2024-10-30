.. _structures-couldbestatic:

.. _could-be-a-static-variable:

Could Be A Static Variable
++++++++++++++++++++++++++

  This global is only used in one function or method. It may be transformed into a '`static <https://www.php.net/manual/en/language.oop5.static.php>`_' variable, instead of global. This allows you to keep the value between call to the function, but will not be accessible outside this function.

.. code-block:: php
   
   <?php
   function foo( ) {
       static $variableIsReservedForX; // only accessible within foo( ), even between calls.
       global $variableIsGlobal;       //      accessible everywhere in the application
   }
   ?>
Connex PHP features
-------------------

  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_
  + `static-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/static-variable.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldBeStatic                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolphin-structures-couldbestatic`, :ref:`case-contao-structures-couldbestatic`                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


