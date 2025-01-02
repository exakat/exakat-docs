.. _structures-noreferenceonleft:

.. _no-reference-on-left-side:

No Reference On Left Side
+++++++++++++++++++++++++

.. meta::
	:description:
		No Reference On Left Side: Do not use references as the right element in an assignation.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Reference On Left Side
	:twitter:description: No Reference On Left Side: Do not use references as the right element in an assignation
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Reference On Left Side
	:og:type: article
	:og:description: Do not use references as the right element in an assignation
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Reference On Left Side.html
	:og:locale: en
Do not use references as the right element in an assignation. 
This is the case for most situations : addition, multiplication, bitshift, logical, power, concatenation.
Note that PHP won't compile the code if the operator is a short operator (+=, .=, etc.), nor if the & is on the right side of the operator.

.. code-block:: php
   
   <?php
   
   $b = 2;
   $c = 3;
   
   $a = &$b + $c;
   // $a === 2 === $b;
   
   $a = $b + $c;
   // $a === 5
   
   ?>

See also `References Explained <https://www.php.net/manual/en/language.references.php>`_ and `Operator Precedence <https://www.php.net/manual/en/language.operators.precedence.php>`_.

Connex PHP features
-------------------

  + `reference <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoReferenceOnLeft                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.5                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


