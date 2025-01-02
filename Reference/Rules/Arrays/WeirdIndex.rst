.. _arrays-weirdindex:

.. _weird-array-index:

Weird Array Index
+++++++++++++++++

.. meta::
	:description:
		Weird Array Index: Array index that looks weird.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Weird Array Index
	:twitter:description: Weird Array Index: Array index that looks weird
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Weird Array Index
	:og:type: article
	:og:description: Array index that looks weird
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Weird Array Index.html
	:og:locale: en
Array index that looks weird. Arrays index may be string or integer, but some strings looks weird.

In particular, strings that include terminal white spaces, often leads to missed values.
Although this is rare `error <https://www.php.net/error>`_, and often easy to spot, it is also very hard to find when it strikes.

.. code-block:: php
   
   <?php
   
   $array = ['a ' => 1, 'b' => 2, 'c' => 3];
   
   // Later in the code
   
   //Notice: Undefined index: a in /Users/famille/Desktop/analyzeG3/test.php on line 8
   echo $array['a'];
   
   //Notice: Undefined index: b  in /Users/famille/Desktop/analyzeG3/test.php on line 10
   // Note that the space is visible, but easy to miss
   echo $array['b '];
   
   // all fine here
   echo $array['c'];
   
   ?>
Connex PHP features
-------------------

  + `index <https://php-dictionary.readthedocs.io/en/latest/dictionary/index.ini.html>`_


Suggestions
___________

* Remove white spaces when using strings as array index.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/WeirdIndex                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


