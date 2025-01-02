.. _php-usortsorting:

.. _usort-sorting-in-php-7.0:

Usort Sorting In PHP 7.0
++++++++++++++++++++++++

.. meta::
	:description:
		Usort Sorting In PHP 7.0: Usort(), uksort() and uasort() behavior has changed in PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Usort Sorting In PHP 7.0
	:twitter:description: Usort Sorting In PHP 7.0: Usort(), uksort() and uasort() behavior has changed in PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Usort Sorting In PHP 7.0
	:og:type: article
	:og:description: Usort(), uksort() and uasort() behavior has changed in PHP 7
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Usort Sorting In PHP 7.0.html
	:og:locale: en
`Usort() <https://www.php.net/usort>`_, `uksort() <https://www.php.net/uksort>`_ and `uasort() <https://www.php.net/uasort>`_ behavior has changed in PHP 7. Values that are equals (based on the user-provided method) may be sorted differently than in PHP 5. 

If this sorting is important, it is advised to add extra comparison in the user-function and avoid returning 0 (thus, depending on default implementation). 
In PHP 5, the results is :::

   
   Array
   (
       [0] => 3
       [1] => 4
       [2] => 2
       [3] => 6
   )
   


in PHP 7, the `result <https://www.php.net/result>`_ is :::

   
   Array
   (
       [0] => 2
       [1] => 4
       [2] => 3
       [3] => 6
   )
   


.. code-block:: php
   
   <?php
   
   $a = [ 2, 4, 3, 6];
   
   function noSort($a) { return $a > 5; }
   
   usort($a, 'noSort');
   print_r($a);
   
   ?>

See also `Sort order of equal elements <https://www.php.net/manual/en/migration70.incompatible.php#migration70.incompatible.other.sort-order>`_.

Connex PHP features
-------------------

  + `sort <https://php-dictionary.readthedocs.io/en/latest/dictionary/sort.ini.html>`_


Suggestions
___________

* Make sure the sorting function doesn't generate any values of the same order.
* Add an extra order branch to avoid values of the same order.
* Spot the values of the same order after the sort, and sort them again, independently.




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/UsortSorting                                                                                                                     |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Medium                                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


