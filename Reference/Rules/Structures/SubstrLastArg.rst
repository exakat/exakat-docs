.. _structures-substrlastarg:


.. _drop-substr-last-arg:

Drop Substr Last Arg
++++++++++++++++++++

.. meta::
	:description:
		Drop Substr Last Arg: Substr() works till the end of the string when the last argument is omitted.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Drop Substr Last Arg
	:twitter:description: Drop Substr Last Arg: Substr() works till the end of the string when the last argument is omitted
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Drop Substr Last Arg
	:og:type: article
	:og:description: Substr() works till the end of the string when the last argument is omitted
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Drop Substr Last Arg.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SubstrLastArg.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SubstrLastArg.html","name":"Drop Substr Last Arg","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Substr() works till the end of the string when the last argument is omitted","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Drop Substr Last Arg.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`Substr() <https://www.php.net/substr>`_ works till the end of the string when the last argument is omitted. There is no need to calculate string size to make this work.

.. code-block:: php
   
   <?php
   
   $string = 'abcdef';
   
   // Extract the end of the string
   $cde = substr($string, 2);
   
   // Too much work
   $cde = substr($string, 2, strlen($string));
   
   ?>

Suggestions
___________

* Use negative length
* Omit the last argument to get the string till its end




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SubstrLastArg                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-suitecrm-structures-substrlastarg`, :ref:`case-tine20-structures-substrlastarg`                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


