.. _performances-mbstringinloop:

.. _no-mb\_substr-in-loop:

No mb_substr In Loop
++++++++++++++++++++

.. meta\:\:
	:description:
		No mb_substr In Loop: Do not use loops on mb_substr().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No mb_substr In Loop
	:twitter:description: No mb_substr In Loop: Do not use loops on mb_substr()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No mb_substr In Loop
	:og:type: article
	:og:description: Do not use loops on mb_substr()
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Performances/MbStringInLoop.html
	:og:locale: en
  Do not use loops on `mb_substr() <https://www.php.net/mb_substr>`_. 

`mb_substr() <https://www.php.net/mb_substr>`_ always starts at the beginning of the string to search for the nth char, and recalculate everything. This means that the first iterations are as fast as `substr() <https://www.php.net/substr>`_ (for comparison), while the longer the string, the slower `mb_substr() <https://www.php.net/mb_substr>`_.

The recommendation is to use `preg_split() <https://www.php.net/preg_split>`_ with the `u` option, to split the string into an array. This save multiple recalculations.

.. code-block:: php
   
   <?php
   
   // Split the string by characters
   $array = preg_split('//u', $string, -1, PREG_SPLIT_NO_EMPTY);
   foreach($array as $c) {
       doSomething($c);
   }
   
   // Slow version
   $nb = mb_strlen($mb);
   for($i = 0; $i < $nb; ++$i) {
       // Fetch a character
       $c = mb_substr($string, $i, 1);
       doSomething($c);
   }
   
   ?>

See also `Optimization: How I made my PHP code run 100 times faster <https://mike42.me/blog/2018-06-how-i-made-my-php-code-run-100-times-faster>`_ and `How to iterate UTF-8 string in PHP? <https://stackoverflow.com/questions/3666306/how-to-iterate-utf-8-string-in-php>`_.

Connex PHP features
-------------------

  + `csv <https://php-dictionary.readthedocs.io/en/latest/dictionary/csv.ini.html>`_


Suggestions
___________

* Use preg_split() and loop on its results.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/MbStringInLoop                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.6                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


