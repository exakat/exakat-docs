.. _structures-arraymergeandvariadic:

.. _array\_merge()-and-variadic:

array_merge() And Variadic
++++++++++++++++++++++++++

.. meta::
	:description:
		array_merge() And Variadic: Always check value in variadic before using it with array_merge() and array_merge_recursive().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: array_merge() And Variadic
	:twitter:description: array_merge() And Variadic: Always check value in variadic before using it with array_merge() and array_merge_recursive()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: array_merge() And Variadic
	:og:type: article
	:og:description: Always check value in variadic before using it with array_merge() and array_merge_recursive()
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/ArrayMergeAndVariadic.html
	:og:locale: en
Always check value in variadic before using it with `array_merge() <https://www.php.net/array_merge>`_ and `array_merge_recursive() <https://www.php.net/array_merge_recursive>`_.

Before PHP 7.4, `array_merge() <https://www.php.net/array_merge>`_ and `array_merge_recursive() <https://www.php.net/array_merge_recursive>`_ would complain when no argument was provided. As such, using the spread operator `...` on an empty `array() <https://www.php.net/array>`_ would yield no argument, and an `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   $b = array_merge(...$x);
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/array_merge%28%29+expects+at+least+1+parameter%2C+0+given.html>`_



Connex PHP features
-------------------

  + `variadic <https://php-dictionary.readthedocs.io/en/latest/dictionary/variadic.ini.html>`_


Suggestions
___________

* Add a check to the spread variable to ensure it is not empty
* Append an empty array to to the spread variable to ensure it is not empty




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ArrayMergeAndVariadic                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


