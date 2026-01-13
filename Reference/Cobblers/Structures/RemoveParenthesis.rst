.. _structures-removeparenthesis:

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


