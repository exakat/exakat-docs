.. _structures-blindvariableusedbeyondloop:

.. _blind-variable-used-beyond-loop:

Blind Variable Used Beyond Loop
+++++++++++++++++++++++++++++++

  `Foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loops defines variables, which are traditionally used only inside the loop block. Using them beyond that limit often leads to surprises.

.. code-block:: php
   
   <?php
   
   foreach($a as $b => $c) {
   	echo "$b : $c\n";
   }
   // $b is set inside the loop, but used beyond
   $max = $b;
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/BlindVariableUsedBeyondLoop                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


