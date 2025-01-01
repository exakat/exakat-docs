.. _structures-blindvariableusedbeyondloop:

.. _blind-variable-used-beyond-loop:

Blind Variable Used Beyond Loop
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		Blind Variable Used Beyond Loop: Foreach() loops defines variables, which are traditionally used only inside the loop block.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Blind Variable Used Beyond Loop
	:twitter:description: Blind Variable Used Beyond Loop: Foreach() loops defines variables, which are traditionally used only inside the loop block
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Blind Variable Used Beyond Loop
	:og:type: article
	:og:description: Foreach() loops defines variables, which are traditionally used only inside the loop block
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/BlindVariableUsedBeyondLoop.html
	:og:locale: en
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


