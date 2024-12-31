.. _arrays-gettinglastelement:

.. _getting-last-element:

Getting Last Element
++++++++++++++++++++

.. meta\:\:
	:description:
		Getting Last Element: Getting the last element of an array relies on array_key_last().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Getting Last Element
	:twitter:description: Getting Last Element: Getting the last element of an array relies on array_key_last()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Getting Last Element
	:og:type: article
	:og:description: Getting the last element of an array relies on array_key_last()
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Arrays/GettingLastElement.html
	:og:locale: en
  Getting the last element of an array relies on `array_key_last() <https://www.php.net/array_key_last>`_.

`array_key_last() <https://www.php.net/array_key_last>`_ was added in PHP 7.3. Before that, other ways had to be used, such as reaching the ``count() - 1`` elements, or via ``array_pop(`array_keys()) <https://www.php.net/array_keys>`_``.

.. code-block:: php
   
   <?php
   
   $array = ['a' => 1, 'b' => 2, 'c' => 3];
   
   // Best solutions, by far
   $last = $array[array_key_last($array)];
   
   // Best solutions, just as fast as each other
   $last = $array[count($array) - 1];
   $last = end($array);
   
   // Bad solutions
   
   // popping, but restoring the value. 
   $last = array_pop($array);
   $array[] = $last; 
   
   // array_unshift would be even worse
   
   // reversing array
   $last = array_reverse($array)[0];
   
   // slicing the array
   $last = array_slice($array, -1)[0]',
   $last = current(array_slice($array, -1));
   );
   
   ?>
Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Use PHP native function : array_key_last(), when using PHP 7.4 and later
* Use PHP native function : array_pop()
* Organise the code to put the last element in the first position (array_unshift() instead of append operator [])




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/GettingLastElement                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.0                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-thelia-arrays-gettinglastelement`                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


