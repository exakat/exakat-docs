.. _functions-useconstantasarguments:

.. _use-constant-as-arguments:

Use Constant As Arguments
+++++++++++++++++++++++++

  Some methods and functions are defined to be used with constants as arguments. Those constants are made to be meaningful and readable, keeping the code maintenable. It is recommended to use such constants as soon as they are documented.
Here is the list of functions that use a unique PHP constant as argument : 

+ `array_change_key_case() <https://www.php.net/array_change_key_case>`_
+ `array_multisort() <https://www.php.net/array_multisort>`_
+ `array_unique() <https://www.php.net/array_unique>`_
+ `count() <https://www.php.net/count>`_
+ `dns_get_record() <https://www.php.net/dns_get_record>`_
+ `easter_days() <https://www.php.net/easter_days>`_
+ `extract() <https://www.php.net/extract>`_
+ `filter_input() <https://www.php.net/filter_input>`_
+ `filter_var() <https://www.php.net/filter_var>`_
+ `fseek() <https://www.php.net/fseek>`_
+ `get_html_translation_table() <https://www.php.net/get_html_translation_table>`_
+ `gmp_div_q() <https://www.php.net/gmp_div_q>`_
+ `gmp_div_qr() <https://www.php.net/gmp_div_qr>`_
+ `gmp_div_r() <https://www.php.net/gmp_div_r>`_
+ `html_entity_decode() <https://www.php.net/html_entity_decode>`_
+ `htmlspecialchars_decode() <https://www.php.net/htmlspecialchars_decode>`_
+ `http_build_query() <https://www.php.net/http_build_query>`_
+ `http_parse_cookie() <https://www.php.net/http_parse_cookie>`_
+ `http_parse_params() <https://www.php.net/http_parse_params>`_
+ `http_redirect() <https://www.php.net/http_redirect>`_
+ `http_support() <https://www.php.net/http_support>`_
+ `parse_ini_file() <https://www.php.net/parse_ini_file>`_
+ `parse_ini_string() <https://www.php.net/parse_ini_string>`_
+ `parse_url() <https://www.php.net/parse_url>`_
+ `pathinfo() <https://www.php.net/pathinfo>`_
+ `pg_select() <https://www.php.net/pg_select>`_
+ `posix_access() <https://www.php.net/posix_access>`_
+ `round() <https://www.php.net/round>`_
+ `scandir() <https://www.php.net/scandir>`_
+ `socket_read() <https://www.php.net/socket_read>`_
+ `str_pad() <https://www.php.net/str_pad>`_
+ `trigger_error() <https://www.php.net/trigger_error>`_

Here is the list of functions that use a combination of PHP native constants as argument.

+ `arsort() <https://www.php.net/arsort>`_
+ `asort() <https://www.php.net/asort>`_
+ `error_reporting() <https://www.php.net/error_reporting>`_
+ `filter_input() <https://www.php.net/filter_input>`_
+ `filter_var() <https://www.php.net/filter_var>`_
+ `get_html_translation_table() <https://www.php.net/get_html_translation_table>`_
+ `htmlentities() <https://www.php.net/htmlentities>`_
+ `htmlspecialchars() <https://www.php.net/htmlspecialchars>`_
+ `http_build_url() <https://www.php.net/http_build_url>`_
+ `jdtojewish() <https://www.php.net/jdtojewish>`_
+ `krsort() <https://www.php.net/krsort>`_
+ `ksort() <https://www.php.net/ksort>`_
+ `pg_result_status() <https://www.php.net/pg_result_status>`_
+ `phpcredits() <https://www.php.net/phpcredits>`_
+ `phpinfo() <https://www.php.net/phpinfo>`_
+ `preg_grep() <https://www.php.net/preg_grep>`_
+ `preg_match() <https://www.php.net/preg_match>`_
+ `preg_split() <https://www.php.net/preg_split>`_
+ `rsort() <https://www.php.net/rsort>`_
+ runkit_import()
+ `sort() <https://www.php.net/sort>`_
+ `stream_socket_client() <https://www.php.net/stream_socket_client>`_
+ `stream_socket_server() <https://www.php.net/stream_socket_server>`_

.. code-block:: php
   
   <?php
   
   // Turn off all error reporting
   // 0 and -1 are accepted 
   error_reporting(0);
   
   // Report simple running errors
   error_reporting(E_ERROR | E_WARNING | E_PARSE);
   
   // The first argument can be one of INPUT_GET, INPUT_POST, INPUT_COOKIE, INPUT_SERVER, or INPUT_ENV.
   $search_html = filter_input(INPUT_GET, 'search', FILTER_SANITIZE_SPECIAL_CHARS);
   
   // sort accepts one of SORT_REGULAR, SORT_NUMERIC, SORT_STRING, SORT_LOCALE_STRING, SORT_NATURAL
   // SORT_FLAG_CASE may be added, and combined with SORT_STRING or SORT_NATURAL
   sort($fruits);
   
   ?>

Suggestions
___________

* Use PHP native constants, whenever possible, instead of nondescript literals.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UseConstantAsArguments                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tikiwiki-functions-useconstantasarguments`, :ref:`case-shopware-functions-useconstantasarguments`                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


