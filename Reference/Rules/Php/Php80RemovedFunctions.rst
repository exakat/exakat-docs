.. _php-php80removedfunctions:

.. _php-8.0-removed-functions:

PHP 8.0 Removed Functions
+++++++++++++++++++++++++

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


Suggestions
___________

* Remove the code related to those functions




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php80RemovedFunctions                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`                                                                                |
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
| Features     | native-function                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


