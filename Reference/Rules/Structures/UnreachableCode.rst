.. _structures-unreachablecode:

.. _unreachable-code:

Unreachable Code
++++++++++++++++

  Code may be unreachable, because other instructions prevent its reaching. 

For example, it be located after throw, return, `exit() <https://www.www.php.net/exit>`_, `die() <https://www.php.net/die>`_, goto, `break <https://www.php.net/manual/en/control-structures.break.php>`_ or `continue <https://www.php.net/manual/en/control-structures.continue.php>`_ : this way, it cannot be reached, as the previous instruction will divert the `engine <https://www.php.net/engine>`_ to another part of the code. 


.. code-block:: php
   
   <?php
   
   function foo() {
       $a++;
       return $a;
       $b++;      // $b++ can't be reached;
   }
   
   function bar() {
       if ($a) {
           return $a;
       } else {
           return $b;
       }
       $b++;      // $b++ can't be reached;
   }
   
   foreach($a as $b) {
       $c += $b;
       if ($c > 10) {
           continue 1;
       } else {
           $c--;
           continue;
       }
       $d += $e;   // this can't be reached
   }
   
   $a = 1;
   goto B;
   class foo {}    // Definitions are accessible, but not functioncalls
   B: 
   echo $a;
   
   ?>


This is dead code, that may be removed.

See also `Unreachable code <https://en.wikipedia.org/wiki/Unreachable_code>`_.


Suggestions
___________

* Remove the unreachable code
* Remove the blocking expression, and let the rest of the code execute




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UnreachableCode                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Dead code <ruleset-Dead-code>`, :ref:`Suggestions <ruleset-Suggestions>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | unreachable-code                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-dead-code <https://github.com/dseguy/clearPHP/tree/master/rules/no-dead-code.md>`__                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


