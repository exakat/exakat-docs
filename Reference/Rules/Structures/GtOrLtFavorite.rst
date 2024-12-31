.. _structures-gtorltfavorite:

.. _comparisons-orientation:

Comparisons Orientation
+++++++++++++++++++++++

.. meta\:\:
	:description:
		Comparisons Orientation: Maths has two comparisons styles : ``>`` or ``<``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Comparisons Orientation
	:twitter:description: Comparisons Orientation: Maths has two comparisons styles : ``>`` or ``<``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Comparisons Orientation
	:og:type: article
	:og:description: Maths has two comparisons styles : ``>`` or ``<``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/GtOrLtFavorite.html
	:og:locale: en
  Maths has two comparisons styles : ``>`` or ``<``. Both may include equality : ``<=`` and ``>=``.

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same. 

It is recommended to always use the same comparison style.

.. code-block:: php
   
   <?php
   
   // Always compare in the same direction
   if ($a > $c) {
   
   } elseif ($c > $b) {
   
   } else {
       // equality case
   }
   
   // Alterning comparison style lead to harder to read code
   if ($b > 3) {
   
   } elseif ($b < 3) {
   
   }
   
   ?>

See also `Comparison Operators <https://www.php.net/manual/en/language.operators.comparison.php>`_.

Connex PHP features
-------------------

  + `comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/comparison.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/GtOrLtFavorite                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


