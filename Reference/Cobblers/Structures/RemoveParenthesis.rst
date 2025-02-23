.. _structures-removeparenthesis:

.. meta::
	:description:
		Remove Parenthesis: Remove useless parenthesis from return expression.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Remove Parenthesis
	:twitter:description: Remove Parenthesis: Remove useless parenthesis from return expression
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Remove Parenthesis
	:og:type: article
	:og:description: Remove useless parenthesis from return expression
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Cobblers/Structures/RemoveParenthesis.html
	:og:locale: en

.. _remove-parenthesis:

Remove Parenthesis
++++++++++++++++++
Remove useless parenthesis from return expression.

.. _remove-parenthesis-before:

Before
______
.. code-block:: php

   <?php
   function foo() {
       return (1);
   }
   ?>

.. _remove-parenthesis-after:

After
_____
.. code-block:: php

   <?php
   function foo() {
       return 1;
   }
   ?>

.. _remove-parenthesis-suggested-analysis:

Suggested Analysis
__________________

* :ref:`no-parenthesis-for-language-construct`



.. _remove-parenthesis-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/RemoveParenthesis                                                                                            |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


