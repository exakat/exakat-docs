.. _structures-arraymergeonearg:


.. _array\_merge()-with-one-arg:

array_merge() With One Arg
++++++++++++++++++++++++++

.. meta::
	:description:
		array_merge() With One Arg: array_merge() combine several arrays together.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: array_merge() With One Arg
	:twitter:description: array_merge() With One Arg: array_merge() combine several arrays together
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: array_merge() With One Arg
	:og:type: article
	:og:description: array_merge() combine several arrays together
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/array_merge() With One Arg.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayMergeOneArg.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayMergeOneArg.html","name":"array_merge() With One Arg","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 04 Feb 2025 14:25:53 +0000","dateModified":"Tue, 04 Feb 2025 14:25:53 +0000","description":"array_merge() combine several arrays together","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/array_merge() With One Arg.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`array_merge() <https://www.php.net/array_merge>`_ combine several arrays together. It also works with one argument: then, it is only useful when the argument is spread, and contains several arrays. Otherwise, `array_merge() <https://www.php.net/array_merge>`_ returns the array.

.. code-block:: php
   
   <?php
   
   $array  =[[1,2], [3, 4]];
   $new = array_merge($array);
   // $new === $array
   
   // actual usage
   $new = array_merge(...$array);
   // $new = [1,2,3,4];
   
   ?>
Connex PHP features
-------------------

  + `array_merge <https://php-dictionary.readthedocs.io/en/latest/dictionary/array_merge.ini.html>`_


Suggestions
___________

* Add the variadic operator ``...`` before the argument.
* Add the other arguments after this first one.
* Remove the array_merge() calls.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ArrayMergeOneArg                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.7.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


