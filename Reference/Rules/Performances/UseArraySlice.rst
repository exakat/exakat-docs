.. _performances-usearrayslice:

.. _use-array\_slice():

Use array_slice()
+++++++++++++++++

.. meta\:\:
	:description:
		Use array_slice(): Array_slice() is de equivalent of substr() for arrays.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use array_slice()
	:twitter:description: Use array_slice(): Array_slice() is de equivalent of substr() for arrays
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use array_slice()
	:og:type: article
	:og:description: Array_slice() is de equivalent of substr() for arrays
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Performances/UseArraySlice.html
	:og:locale: en
  `Array_slice() <https://www.php.net/array_slice>`_ is de equivalent of `substr() <https://www.php.net/substr>`_ for arrays.

`array_splice() <https://www.php.net/array_splice>`_ is also available, to remove a portion of array inside the array, not at the ends. This has no simple equivalent for strings.

.. code-block:: php
   
   <?php
   
   $array = range(0, 9);
   
   // Extract the 5 first elements
   print_r(array_slice($array, 0, 5));
   
   // Extract the 4 last elements
   print_r(array_slice($array, -4));
   
   // Extract the 2 central elements : 4 and 5
   print_r(array_splice($array, 4, 2));
   
   // slow way to remove the last elementst of an array
   for($i = 0; $i < 4) {
       array_pop($array);
   }
   
   ?>

See also `array_slice <http://www.php.net/array_slice>`_ and `array_splice <http://www.php.net/array_splice>`_.

Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Use array_slice()




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/UseArraySlice                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.5                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


