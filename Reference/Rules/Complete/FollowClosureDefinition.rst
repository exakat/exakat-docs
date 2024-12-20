.. _complete-followclosuredefinition:

.. _follow-closure-definition:

Follow Closure Definition
+++++++++++++++++++++++++

  This command adds DEFINITION link between `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_ and arrow functions definitions and their usage.

Local usage of the `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, in the same scope, are detected. Relayed `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, when they are transmitted to another method for usage, is detected, for one jump.

This also supports first class callable, when the callable is defined in the code code (aka, not with native PHP functions or external libraries).

.. code-block:: php
   
   <?php
   
   function foo() {
       $closure = function () {};
       // Local usage
       echo $closure();
   }
   
   function bar(Closure $x) {
       // relayed usage
       echo $x(); 
   }
   
   
   ?>
Connex PHP features
-------------------

  + `closure <https://php-dictionary.readthedocs.io/en/latest/dictionary/closure.ini.html>`_
  + `arrow-function <https://php-dictionary.readthedocs.io/en/latest/dictionary/arrow-function.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/FollowClosureDefinition                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


