.. _structures-foreachsourcevalue:

.. _overwritten-source-and-value:

Overwritten Source And Value
++++++++++++++++++++++++++++

.. meta::
	:description:
		Overwritten Source And Value: In a foreach(), it is best to keep source and values distinct.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Overwritten Source And Value
	:twitter:description: Overwritten Source And Value: In a foreach(), it is best to keep source and values distinct
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Overwritten Source And Value
	:og:type: article
	:og:description: In a foreach(), it is best to keep source and values distinct
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Overwritten Source And Value.html
	:og:locale: en
In a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_, it is best to keep source and values distinct. Otherwise, they overwrite each other.

Since PHP 7.0, PHP makes a copy of the original source, then works on it. This makes possible to use the same name for the source and the values.
When the source is used as the value, the elements in the array are successively assigned to itself. After the loop, the original array has been replaced by its last element.

The same applies to the index, or to any variable in a `list() <https://www.php.net/list>`_ structure, used in a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_.

.. code-block:: php
   
   <?php
   
   // displays 0-1-2-3-3
   $array = range(0, 3);
   foreach($array as $array) {
       print $array . '-';
   }
   print_r($array);
   
   
   /* displays 0-1-2-3-Array
   (
       [0] => 0
       [1] => 1
       [2] => 2
       [3] => 3
   )
   */
   $array = range(0, 3);
   foreach($array as $v) {
       print $v . '-';
   }
   print_r($array);
   
   ?>
Connex PHP features
-------------------

  + `foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_


Suggestions
___________

* Keep the source, the index and the values distinct




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ForeachSourceValue                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-churchcrm-structures-foreachsourcevalue`, :ref:`case-expressionengine-structures-foreachsourcevalue`         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


