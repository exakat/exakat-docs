.. _classes-swappedarguments:

.. _swapped-arguments:

Swapped Arguments
+++++++++++++++++

  Overwritten methods must be compatible, but argument names is not part of that compatibility.

Methods with the same name, in two classes of the same hierarchy, must be compatible for typehint, default value, reference. The name of the argument is not taken into account when checking such compatibility, at least until PHP 7.4.


.. code-block:: php
   
   <?php
   
   class x {
       function foo($a, $b) {}
       
       function bar($a, $b) {}
   }
   
   class y extends x {
       // foo is compatible (identical) with the above class
       function foo($a, $b) {}
       
       // bar is compatible with the above class, yet, the argument might not receive what they expect.
       function bar($b, $a) {}
   }
   
   ?>


This analysis reports argument lists that differs in ordering. This analysis doesn't report argument lists that also differs in argument names.

Suggestions
___________

* Make sure the names of the argument are in the same order in all classes and interfaces




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/SwappedArguments                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | class                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


