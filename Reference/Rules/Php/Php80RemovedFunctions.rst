.. _php-php80removedfunctions:


.. _php-8.0-removed-functions:

PHP 8.0 Removed Functions
+++++++++++++++++++++++++


.. meta::

	:description:

		PHP 8.0 Removed Functions: The following PHP native functions were deprecated in PHP 8.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: PHP 8.0 Removed Functions

	:twitter:description: PHP 8.0 Removed Functions: The following PHP native functions were deprecated in PHP 8

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: PHP 8.0 Removed Functions

	:og:type: article

	:og:description: The following PHP native functions were deprecated in PHP 8

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP 8.0 Removed Functions.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php80RemovedFunctions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php80RemovedFunctions.html","name":"PHP 8.0 Removed Functions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The following PHP native functions were deprecated in PHP 8","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP 8.0 Removed Functions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The following PHP native functions were deprecated in PHP 8.0, and will be removed in PHP 9.0.

* image2wbmp()
* png2wbmp()
* jpeg2wbmp()
* ldap_sort()
* `hebrevc() <https://www.php.net/hebrevc>`_
* `convert_cyr_string() <https://www.php.net/convert_cyr_string>`_
* `ezmlm_hash() <https://www.php.net/ezmlm_hash>`_
* `money_format() <https://www.php.net/money_format>`_
* `get_magic_quotes_gpc() <https://www.php.net/get_magic_quotes_gpc>`_
* get_magic_quotes_gpc_runtime()
* create_function()
* `each() <https://www.php.net/each>`_
* read_exif_data()
* gmp_random()
* `fgetss() <https://www.php.net/fgetss>`_
* `restore_include_path() <https://www.php.net/restore_include_path>`_
* gzgetss()
* mbregex_encoding()
* mbereg()
* mberegi()
* mbereg_replace()
* mberegi_replace()
* mbsplit()
* mbereg_match()
* mbereg_search()
* mbereg_search_pos()
* mbereg_search_regs()
* mbereg_search_init()
* mbereg_search_getregs()
* mbereg_search_getpos()
* mbereg_search_setpos()

See also `Backward Incompatible Changes <https://www.php.net/manual/en/migration80.incompatible.php#migration80.incompatible>`_.

Connex PHP features
-------------------

  + `native-function <https://php-dictionary.readthedocs.io/en/latest/dictionary/native-function.ini.html>`_


Suggestions
___________

* Remove the code related to those functions




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php80RemovedFunctions                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.8                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


