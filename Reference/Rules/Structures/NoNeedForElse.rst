.. _structures-noneedforelse:

.. _no-need-for-else:

No Need For Else
++++++++++++++++

  Else is not needed when the Then ends with a `break <https://www.php.net/manual/en/control-structures.break.php>`_. A `break <https://www.php.net/manual/en/control-structures.break.php>`_ may be the following keywords : `break <https://www.php.net/manual/en/control-structures.break.php>`_, `continue <https://www.php.net/manual/en/control-structures.continue.php>`_, return, goto. Any of these send the execution somewhere in the code. The else block is then executed as the main sequence, only if the condition fails.

.. code-block:: php
   
   <?php
   
   function foo() {
       // Else may be in the main sequence.
       if ($a1) {
           return $a1;
       } else {
           $a++;
       }
   
       // Same as above, but negate the condition : if (!$a2) { return $a2; }
       if ($a2) {
           $a++;
       } else {
           return $a2;
       }
   
       // This is OK
       if ($a3) {
           return;
       }
   
       // This has no break
       if ($a4) {
           $a++;
       } else {
           $b++;
       }
   
       // This has no else
       if ($a5) {
           $a++;
       }
   }
   ?>

See also `Object Calisthenics, rule # 2 <http://williamdurand.fr/2013/06/03/object-calisthenics/>`_.


Suggestions
___________

* Remove else block, but keep the code




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoNeedForElse                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.4                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | if-then                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-thelia-structures-noneedforelse`, :ref:`case-thinkphp-structures-noneedforelse`                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


