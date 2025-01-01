.. _php-shouldusearraycolumn:

.. _should-use-array\_column():

Should Use array_column()
+++++++++++++++++++++++++

.. meta::
	:description:
		Should Use array_column(): Avoid writing a whole slow loop, and use the native array_column().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Use array_column()
	:twitter:description: Should Use array_column(): Avoid writing a whole slow loop, and use the native array_column()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Use array_column()
	:og:type: article
	:og:description: Avoid writing a whole slow loop, and use the native array_column()
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/ShouldUseArrayColumn.html
	:og:locale: en
Avoid writing a whole slow loop, and use the native `array_column() <https://www.php.net/array_column>`_.

`array_column() <https://www.php.net/array_column>`_ is a native PHP function, that extract a property or a index from a array of object, or a multidimensional array. This prevents the usage of foreach to collect those values.
`array_column() <https://www.php.net/array_column>`_ is faster than `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ (with or without the `isset() <https://www.www.php.net/isset>`_ test) with 3 elements or more, and it is significantly faster beyond 5 elements. Memory consumption is the same.

.. code-block:: php
   
   <?php
   
   $a = array(array('b' => 1), 
              array('b' => 2, 'c' => 3), 
              array(          'c' => 4)); // b doesn't always exists
   
   $bColumn = array_column($a, 'b');
   
   // Slow and cumbersome code
   $bColumn = array();
   foreach($a as $k => $v) {
       if (isset($v['b'])) {
           $bColumn[] = $v['b'];
       }
   }
   
   ?>

See also `[blog] array_column() <https://benramsey.com/projects/array-column/>`_ and preprocess.


Suggestions
___________

* Use array_column(), instead of a foreach()




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ShouldUseArrayColumn                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.2                                                                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+


