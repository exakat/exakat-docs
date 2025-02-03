.. _structures-substrtotrim:

.. _substr-to-trim:

Substr To Trim
++++++++++++++

.. meta::
	:description:
		Substr To Trim: When removing the first or the last character of a string, trim() does a more readable job.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Substr To Trim
	:twitter:description: Substr To Trim: When removing the first or the last character of a string, trim() does a more readable job
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Substr To Trim
	:og:type: article
	:og:description: When removing the first or the last character of a string, trim() does a more readable job
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Substr To Trim.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SubstrToTrim.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SubstrToTrim.html","name":"Substr To Trim","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When removing the first or the last character of a string, trim() does a more readable job","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Substr To Trim.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>When removing the first or the last character of a string, `trim() <https://www.php.net/trim>`_ does a more readable job. 

`trim() <https://www.php.net/trim>`_, `ltrim() <https://www.php.net/ltrim>`_ and `rtrim() <https://www.php.net/rtrim>`_ accept a string as second argument. Those will all be removed from the endings of the string.
`trim() <https://www.php.net/trim>`_ will remove all occurrences of the requested char(). This may remove a loop with `substr() <https://www.php.net/substr>`_, or remove more than is needed. 

`trim() <https://www.php.net/trim>`_ doesn't work with multi-bytes strings, but so does `substr() <https://www.php.net/substr>`_. For that, use `mb_substr() <https://www.php.net/mb_substr>`_, as there isn't any mb_trim() function (so far in PHP 8.2).

.. code-block:: php
   
   <?php
   
   $a = '$drop the dollar'; 
   $b = substr($a, 1); // drop the first char 
   $b = ltrim($a, '$'); // remove the initial '$'s
   
   
   $b = substr($a, 1);     // replace with ltrim()
   
   $b = substr($a, 0, -1); // replace with rtrim()
   
   $b = substr($a, 1, -1); // replace with trim()
   
   ?>

See also `trim <https://www.php.net/manual/en/function.trim.php>`_, `ltrim <https://www.php.net/manual/en/function.ltrim.php>`_ and `rtrim <https://www.php.net/manual/en/function.rtrim.php>`_.


Suggestions
___________

* Replace substr() with trim(), ltrim() or rtrim().




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SubstrToTrim                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.3                                                                                                                   |
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


