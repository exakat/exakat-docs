.. _php-php82newfunctions:

.. _new-functions-in-php-8.2:

New Functions In PHP 8.2
++++++++++++++++++++++++

.. meta::
	:description:
		New Functions In PHP 8.2: New functions are added to new PHP version.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: New Functions In PHP 8.2
	:twitter:description: New Functions In PHP 8.2: New functions are added to new PHP version
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: New Functions In PHP 8.2
	:og:type: article
	:og:description: New functions are added to new PHP version
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/Php82NewFunctions.html
	:og:locale: en
New functions are added to new PHP version.

The following functions are now native functions in PHP 8.2. It is compulsory to rename any custom function that was created in older versions. One alternative is to move the function to a custom namespace, and update the use list at the beginning of the script. 

* `curl_upkeep() <https://www.php.net/curl_upkeep>`_
* `mysqli_execute_query() <https://www.php.net/mysqli_execute_query>`_
* `odbc_connection_string_is_quoted() <https://www.php.net/odbc_connection_string_is_quoted>`_
* `odbc_connection_string_should_quote() <https://www.php.net/odbc_connection_string_should_quote>`_
* `odbc_connection_string_quote() <https://www.php.net/odbc_connection_string_quote>`_
* `ini_parse_quantity() <https://www.php.net/ini_parse_quantity>`_
* `memory_reset_peak_usage() <https://www.php.net/memory_reset_peak_usage>`_
* `sodium_crypto_stream_xchacha20_xor_ic() <https://www.php.net/sodium_crypto_stream_xchacha20_xor_ic>`_

.. code-block:: php
   
   <?php
   
   // Such function will not be possible in PHP 8.2 anymore
   function memory_reset_peak_usage() {}
   
   ?>
Connex PHP features
-------------------

  + `function <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `native <https://php-dictionary.readthedocs.io/en/latest/dictionary/native.ini.html>`_


Suggestions
___________

* Move custom functions with the same name to a new namespace
* Change the name of any custom functions with the same name
* Add a condition to the functions definition to avoid conflict




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php82NewFunctions                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.0                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.2 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


