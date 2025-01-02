.. _php-listwithappends:

.. _list-with-array-appends:

List With Array Appends
+++++++++++++++++++++++

.. meta::
	:description:
		List With Array Appends: List() behavior has changed in PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: List With Array Appends
	:twitter:description: List With Array Appends: List() behavior has changed in PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: List With Array Appends
	:og:type: article
	:og:description: List() behavior has changed in PHP 7
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/List With Array Appends.html
	:og:locale: en
`List() <https://www.php.net/list>`_ behavior has changed in PHP 7.0 and it has impact on the indexing when list is used with the [] operator. 

The appended values are created in the same order than in the syntax, while in PHP 5.6, it is in the reverse order. 
In PHP 7.0, results are :::

   
   Array
   (
       [0] => 1
       [1] => 2
       [2] => 3
   )
   


In PHP 5.6, results are :::

   
   Array
   (
       [0] => 3
       [1] => 2
       [2] => 1
   )
   


.. code-block:: php
   
   <?php
   
   $x = array();
   list($x[], $x[], $x[]) = [1, 2, 3];
   
   print_r($x);
   
   ?>
Connex PHP features
-------------------

  + `list <https://php-dictionary.readthedocs.io/en/latest/dictionary/list.ini.html>`_
  + `append <https://php-dictionary.readthedocs.io/en/latest/dictionary/append.ini.html>`_


Suggestions
___________

* Refactor code to avoid using append in a list() call




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/ListWithAppends                                                                                                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


