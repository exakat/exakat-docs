.. _functions-oneletterfunctions:

.. _one-letter-functions:

One Letter Functions
++++++++++++++++++++

  One letter functions seems to be really short for a meaningful name. This may happens for very high usage functions, so as to keep code short, but such functions should be rare.

.. code-block:: php
   
   <?php
   
   // Always use a meaningful name 
   function addition($a, $b) {
       return $a + $b;
   }
   
   // One letter functions are rarely meaningful
   function f($a, $b) {
       return $a + $b;
   }
   
   ?>
Connex PHP features
-------------------

  + `function <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `semantics <https://php-dictionary.readthedocs.io/en/latest/dictionary/semantics.ini.html>`_


Suggestions
___________

* Use full names for functions
* Remove the function name altogether : use a closure




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/OneLetterFunctions                                                                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>`, :ref:`Semantics <ruleset-Semantics>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-thinkphp-functions-oneletterfunctions`, :ref:`case-cleverstyle-functions-oneletterfunctions`                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


