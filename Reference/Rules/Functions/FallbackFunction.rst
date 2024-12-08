.. _functions-fallbackfunction:

.. _fallback-function:

Fallback Function
+++++++++++++++++

  This rule reports functions that are called with its name alone, and whose definition is in the global scope. Such syntax relies on the fallback mechanism of PHP, which search for functions in the local namespace, then in the global namespace, before failing.

.. code-block:: php
   
   <?php
   
   namespace {
       // global definition
       function foo() {}
   }
   
   namespace Bar {
       // local definition
       function foo2() {}
       
       foo(); // definition is in the global namespace
       foo2(); // definition is in the Bar namespace
   }
   
   ?>

See also `Using namespaces: fallback to global function/constant <https://www.php.net/manual/en/language.namespaces.fallback.php>`_.

Connex PHP features
-------------------

  + `function <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `fallback-function <https://php-dictionary.readthedocs.io/en/latest/dictionary/fallback-function.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/FallbackFunction                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


