.. _structures-strposcompare:

.. _strpos()-like-comparison:

Strpos()-like Comparison
++++++++++++++++++++++++

.. meta\:\:
	:description:
		Strpos()-like Comparison: The result of that function may be mistaken with an error.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Strpos()-like Comparison
	:twitter:description: Strpos()-like Comparison: The result of that function may be mistaken with an error
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Strpos()-like Comparison
	:og:type: article
	:og:description: The result of that function may be mistaken with an error
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/StrposCompare.html
	:og:locale: en
  The `result <https://www.php.net/result>`_ of that function may be mistaken with an `error <https://www.php.net/error>`_.

`strpos() <https://www.php.net/strpos>`_, along with several PHP native functions, returns a string position, starting at 0, or false, in case of failure. 
It is recommended to check the `result <https://www.php.net/result>`_ of `strpos() <https://www.php.net/strpos>`_ with === or !==, so as to avoid confusing 0 and false. 

This analyzer list all the `strpos() <https://www.php.net/strpos>`_-like functions that are directly compared with == or !=. `preg_match() <https://www.php.net/preg_match>`_, when its first argument is a literal, is omitted : this function only returns `NULL <https://www.php.net/manual/en/language.types.null.php>`_ in case of regex `error <https://www.php.net/error>`_. 

The full list is the following : 
* `array_search() <https://www.php.net/array_search>`_
* `collator_compare() <https://www.php.net/collator_compare>`_
* `collator_get_sort_key() <https://www.php.net/collator_get_sort_key>`_
* `current() <https://www.php.net/current>`_
* `fgetc() <https://www.php.net/fgetc>`_
* `file_get_contents() <https://www.php.net/file_get_contents>`_
* `file_put_contents() <https://www.php.net/file_put_contents>`_
* `fread() <https://www.php.net/fread>`_
* `iconv_strpos() <https://www.php.net/iconv_strpos>`_
* `iconv_strrpos() <https://www.php.net/iconv_strrpos>`_
* `imagecolorallocate() <https://www.php.net/imagecolorallocate>`_
* `imagecolorallocatealpha() <https://www.php.net/imagecolorallocatealpha>`_
* `mb_strlen() <https://www.php.net/mb_strlen>`_
* `next() <https://www.php.net/next>`_
* `pcntl_getpriority() <https://www.php.net/pcntl_getpriority>`_
* `preg_match() <https://www.php.net/preg_match>`_
* `prev() <https://www.php.net/prev>`_
* `readdir() <https://www.php.net/readdir>`_
* `stripos() <https://www.php.net/stripos>`_
* `strpos() <https://www.php.net/strpos>`_
* `strripos() <https://www.php.net/strripos>`_
* `strrpos() <https://www.php.net/strrpos>`_
* `strtok() <https://www.php.net/strtok>`_
* `curl_exec() <https://www.php.net/curl_exec>`_

In PHP 8.0, `str_contains() <https://www.php.net/str_contains>`_ will do the expected job of `strpos() <https://www.php.net/strpos>`_, with less confusion.

.. code-block:: php
   
   <?php
   
   // This is the best comparison
   if (strpos($string, 'a') === false) { }
   
   // This is OK, as 2 won't be mistaken with false
   if (strpos($string, 'a') == 2) { }
   
   // strpos is one of the 26 functions that may behave this way
   if (preg_match($regex, $string)) { } 
   
   // This works like above, catching the value for later reuse
   if ($a = strpos($string, 'a')) { }
   
   // This misses the case where 'a' is the first char of the string
   if (strpos($string, 'a')) { }
   
   // This misses the case where 'a' is the first char of the string, just like above
   if (strpos($string, 'a') == 0) { }
   
   ?>

See also `strpos not working correctly <https://bugs.php.net/bug.php?id=52198>`_.

Connex PHP features
-------------------

  + `strict-comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/strict-comparison.ini.html>`_


Suggestions
___________

* Use identity comparisons, for 0 values : === instead of ==, etc.
* Compare with other exact values than 0 : strpos() == 2
* Use str_contains()




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/StrposCompare                                                                                                                                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `strict-comparisons <https://github.com/dseguy/clearPHP/tree/master/rules/strict-comparisons.md>`__                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-piwigo-structures-strposcompare`, :ref:`case-thelia-structures-strposcompare`                                                                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


