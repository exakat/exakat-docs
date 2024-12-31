.. _performances-makeonecall:

.. _make-one-call-with-array:

Make One Call With Array
++++++++++++++++++++++++

.. meta\:\:
	:description:
		Make One Call With Array: Avoid calling the same functions several times by batching the calls with arrays.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Make One Call With Array
	:twitter:description: Make One Call With Array: Avoid calling the same functions several times by batching the calls with arrays
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Make One Call With Array
	:og:type: article
	:og:description: Avoid calling the same functions several times by batching the calls with arrays
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Performances/MakeOneCall.html
	:og:locale: en
  Avoid calling the same functions several times by batching the calls with arrays.

Calling the same function to chain modifications is slower than calling the same function once, with all the transformations at the same time. Some PHP functions accept scalars or arrays, and using the later is more efficient.
Potential replacements : 

+--------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| Function                                                                 | Replacement                                                                         |
+--------------------------------------------------------------------------+-------------------------------------------------------------------------------------+
| `str_replace() <https://www.php.net/str_replace>`_                       | `str_replace() <https://www.php.net/str_replace>`_                                  |
| `str_ireplace() <https://www.php.net/str_ireplace>`_                     | `str_replace() <https://www.php.net/str_replace>`_                                  |
| `substr_replace() <https://www.php.net/substr_replace>`_                 | `substr_replace() <https://www.php.net/substr_replace>`_                            |
| `preg_replace() <https://www.php.net/preg_replace>`_                     | `preg_replace() <https://www.php.net/preg_replace>`_                                |
| `preg_replace_callback() <https://www.php.net/preg_replace_callback>`_   | `preg_replace_callback_array() <https://www.php.net/preg_replace_callback_array>`_  |
+--------------------------------------------------------------------------+-------------------------------------------------------------------------------------+


.. code-block:: php
   
   <?php
   
   $string = 'abcdef'; 
   
   //str_replace() accepts arrays as arguments
   $string = str_replace( ['a', 'b', 'c'],
                          ['A', 'B', 'C'],
                          $string);
   
   // Too many calls to str_replace
   $string = str_replace( 'a', 'A', $string);
   $string = str_replace( 'b', 'B', $string);
   $string = str_replace( 'c', 'C', $string);
   
   // Too many nested calls to str_replace
   $string = str_replace( 'a', 'A', str_replace( 'b', 'B', str_replace( 'c', 'C', $string)));
   
   ?>
Connex PHP features
-------------------

  + `csv <https://php-dictionary.readthedocs.io/en/latest/dictionary/csv.ini.html>`_


Suggestions
___________

* Use str_replace() with arrays as arguments.
* Use preg_replace() with arrays as arguments.
* Use preg_replace_callback() for merging multiple complex calls.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/MakeOneCall                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-humo-gen-performances-makeonecall`, :ref:`case-edusoho-performances-makeonecall`                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


