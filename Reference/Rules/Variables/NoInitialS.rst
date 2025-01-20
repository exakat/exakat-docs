.. _variables-noinitials:

.. _no-initial-s-in-variable-names:

No Initial S In Variable Names
++++++++++++++++++++++++++++++

.. meta::
	:description:
		No Initial S In Variable Names: The initial capital S in a variable name, may easily be mistaken with the dollar sign.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Initial S In Variable Names
	:twitter:description: No Initial S In Variable Names: The initial capital S in a variable name, may easily be mistaken with the dollar sign
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Initial S In Variable Names
	:og:type: article
	:og:description: The initial capital S in a variable name, may easily be mistaken with the dollar sign
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Initial S In Variable Names.html
	:og:locale: en
The initial capital S in a variable name, may easily be mistaken with the dollar sign. This rules reports all variables that use a capital S as first letter after the dollar sign, to avoid this problem.

.. code-block:: php
   
   <?php
   
   $$ocket = $Socket;
   
   ?>
Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_
  + `readability <https://php-dictionary.readthedocs.io/en/latest/dictionary/readability.ini.html>`_


Suggestions
___________

* Avoid using an initial capital S in variable and static property names.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/NoInitialS                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
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


