.. _structures-switchtomatch:

.. _switch-to-match:

Switch To Match
+++++++++++++++
Transforms a switch() into a match() expression.

The switch() syntax must have each of the cases assigning the same variable (or similar). There should not be any other operation, besides break;



.. _switch-to-match-before:

Before
______
.. code-block:: php

   <?php
       switch($a) {
           case 1: 
               $b = '1';
               break;
           case 2: 
               $b = '3';
               break;
           default:  
               $b = '0';
               break; 
       }
   ?>
   

.. _switch-to-match-after:

After
_____
.. code-block:: php

   <?php
       $b = match($a) {
           1 => '1',
           2 => '3',
           default => '0'
       };
   ?>
   

.. _switch-to-match-suggested-analysis:

Suggested Analysis
__________________

* :ref:`could-use-match`

.. _switch-to-match-related-cobbler:

Related Cobblers
________________

* :ref:`post-to-pre-plusplus`

.. _switch-to-match-reverse-cobbler:

Reverse Cobbler
_______________

* :ref:`remove-instructions`



.. _switch-to-match-specs:

Specs
_____

+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Short Name     | Structures/SwitchToMatch                                                                                                |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat version | 2.3.0                                                                                                                   |
+----------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in   | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+----------------+-------------------------------------------------------------------------------------------------------------------------+


