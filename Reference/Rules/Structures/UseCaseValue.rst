.. _structures-usecasevalue:

.. _use-the-case-value:

Use The Case Value
++++++++++++++++++

.. meta::
	:description:
		Use The Case Value: When switch() has branched to the right case, the value of the switched variable is known : it is the case.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use The Case Value
	:twitter:description: Use The Case Value: When switch() has branched to the right case, the value of the switched variable is known : it is the case
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use The Case Value
	:og:type: article
	:og:description: When switch() has branched to the right case, the value of the switched variable is known : it is the case
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use The Case Value.html
	:og:locale: en
When `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ has branched to the right case, the value of the switched variable is known : it is the case.

This doesn't work with complex expression cases, nor with default.

.. code-block:: php
   
   <?php
   
   switch($a) {
       case 'a' : 
           // $a == 'a';
           echo $a;
           break;
           
       case 'b' : 
           // $a == 'b';
           echo 'b';
           break;
   }
   
   ?>

Suggestions
___________

* Use the literal value in the case, to avoid unnecessary computation.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseCaseValue                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


