.. _structures-strormbfavorite:


.. _mono-or-multibytes-favorite:

Mono Or Multibytes Favorite
+++++++++++++++++++++++++++

.. meta::
	:description:
		Mono Or Multibytes Favorite: PHP handles strings wity bytes, and also support multibytes with the mbstring extension.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mono Or Multibytes Favorite
	:twitter:description: Mono Or Multibytes Favorite: PHP handles strings wity bytes, and also support multibytes with the mbstring extension
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mono Or Multibytes Favorite
	:og:type: article
	:og:description: PHP handles strings wity bytes, and also support multibytes with the mbstring extension
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mono Or Multibytes Favorite.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/strOrMbFavorite.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/strOrMbFavorite.html","name":"Mono Or Multibytes Favorite","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP handles strings wity bytes, and also support multibytes with the mbstring extension","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Mono Or Multibytes Favorite.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP handles strings wity bytes, and also support multibytes with the mbstring extension. This analysis reports when the mono or the multi byte version has dominance.

The dominant one is reported when it has over 90% of usage. The remaining cases should be uniformed, so has to make this code consistent.
Sometimes, the same code may make usage of both the versions, depending on the manipulated string. For example, array index as single bytes strings, while user labels as multi-bytes. 

The following functions are used for the analysis : 

+ `mb_substr() <https://www.php.net/mb_substr>`_       =>  `substr()() <https://www.php.net/substr>`_
+ `mb_strtolower() <https://www.php.net/mb_strtolower>`_   =>  `strtolower() <https://www.php.net/strtolower>`_
+ `mb_strtoupper() <https://www.php.net/mb_strtoupper>`_   =>  `strtoupper() <https://www.php.net/strtoupper>`_
+ `mb_strlen() <https://www.php.net/mb_strlen>`_       =>  `strlen() <https://www.php.net/strlen>`_
+ `mb_strpos() <https://www.php.net/mb_strpos>`_       =>  `strpos() <https://www.php.net/strpos>`_
+ `mb_strrpos() <https://www.php.net/mb_strrpos>`_      =>  `strrpos() <https://www.php.net/strrpos>`_
+ `mb_stripos() <https://www.php.net/mb_stripos>`_      =>  `stripos() <https://www.php.net/stripos>`_
+ `mb_strripos() <https://www.php.net/mb_strripos>`_     =>  `strripos() <https://www.php.net/strripos>`_
+ `mb_strstr() <https://www.php.net/mb_strstr>`_       =>  `strstr() <https://www.php.net/strstr>`_
+ `mb_stristr() <https://www.php.net/mb_stristr>`_      =>  `stristr() <https://www.php.net/stristr>`_
+ `mb_strrchr() <https://www.php.net/mb_strrchr>`_      =>  `strrchr() <https://www.php.net/strrchr>`_
+ `mb_substr_count() <https://www.php.net/mb_substr_count>`_ =>  `substr_count() <https://www.php.net/substr_count>`_
+ `mb_chr() <https://www.php.net/mb_chr>`_          =>  `chr() <https://www.php.net/chr>`_
+ `mb_ord() <https://www.php.net/mb_ord>`_          =>  `ord() <https://www.php.net/ord>`_
+ `mb_parse_str() <https://www.php.net/mb_parse_str>`_    =>  `parse_str() <https://www.php.net/parse_str>`_
This rule doesn't detect mb_string overloading, which remplace some of the mono-bytes functions by their mbstring counterpart, without changing the calls in the code.

.. code-block:: php
   
   <?php
   
   echo strlen($string) . PHP_EOL;
   
   echo mb_strlen($string) . PHP_EOL;
   
   ?>

Suggestions
___________

* Make the code uniform by using one of the two versions of string functions




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/strOrMbFavorite                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


