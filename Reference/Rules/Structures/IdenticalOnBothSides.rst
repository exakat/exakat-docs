.. _structures-identicalonbothsides:

.. _identical-on-both-sides:

Identical On Both Sides
+++++++++++++++++++++++

.. meta\:\:
	:description:
		Identical On Both Sides: Operands should be different when comparing or making a logical combination.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Identical On Both Sides
	:twitter:description: Identical On Both Sides: Operands should be different when comparing or making a logical combination
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Identical On Both Sides
	:og:type: article
	:og:description: Operands should be different when comparing or making a logical combination
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/IdenticalOnBothSides.html
	:og:locale: en
  Operands should be different when comparing or making a logical combination. Of course, the value each operand holds may be identical. When the same operand appears on both sides of the expression, the `result <https://www.php.net/result>`_ is know before execution.

.. code-block:: php
   
   <?php
   
   // Trying to confirm consistency
   if ($login == $login) {
       doSomething();
   }
   
   // Works with every operators
   if ($object->login( ) !== $object->login()) {
       doSomething();
   }
   
   if ($sum >= $sum) {
       doSomething();
   }
   
   //
   if ($mask && $mask) {
       doSomething();
   }
   
   if ($mask || $mask) {
       doSomething();
   }
   
   ?>
Connex PHP features
-------------------

  + `if-then <https://php-dictionary.readthedocs.io/en/latest/dictionary/if-then.ini.html>`_


Suggestions
___________

* Remove one of the alternative, and remove the logical link
* Modify one of the alternative, and make it different from the other




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IdenticalOnBothSides                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.8                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpmyadmin-structures-identicalonbothsides`, :ref:`case-humo-gen-structures-identicalonbothsides`                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


