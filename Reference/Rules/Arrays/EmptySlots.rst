.. _arrays-emptyslots:

.. _empty-slots-in-arrays:

Empty Slots In Arrays
+++++++++++++++++++++

.. meta\:\:
	:description:
		Empty Slots In Arrays: PHP allows the last element of an array to be empty.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Empty Slots In Arrays
	:twitter:description: Empty Slots In Arrays: PHP allows the last element of an array to be empty
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Empty Slots In Arrays
	:og:type: article
	:og:description: PHP allows the last element of an array to be empty
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Arrays/EmptySlots.html
	:og:locale: en
  PHP allows the last element of an array to be empty. It doesn't allow any other element to be empty: it should at least be an explicit `NULL <https://www.php.net/manual/en/language.types.null.php>`_  value.

.. code-block:: php
   
   <?php
       $a = array( 1, 2, 3, );
       $b =      [ 4, 5, ];
   ?>
Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/EmptySlots                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


