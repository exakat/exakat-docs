.. _php-php81removedfunctions:

.. _php-8.1-removed-functions:

PHP 8.1 Removed Functions
+++++++++++++++++++++++++

.. meta::
	:description:
		PHP 8.1 Removed Functions: The following PHP native functions were deprecated in PHP 8.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 8.1 Removed Functions
	:twitter:description: PHP 8.1 Removed Functions: The following PHP native functions were deprecated in PHP 8
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 8.1 Removed Functions
	:og:type: article
	:og:description: The following PHP native functions were deprecated in PHP 8
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP 8.1 Removed Functions.html
	:og:locale: en
The following PHP native functions were deprecated in PHP 8.1, and will be removed in PHP 9.0.

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

 

.. code-block:: php
   
   <?php
   
   echo hebrevc(abc);
   
   ?>
Connex PHP features
-------------------

  + `function <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `native-function <https://php-dictionary.readthedocs.io/en/latest/dictionary/native-function.ini.html>`_


Suggestions
___________

* Avoid using those functions anymore




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php81RemovedFunctions                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


