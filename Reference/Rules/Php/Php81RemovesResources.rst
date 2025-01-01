.. _php-php81removesresources:

.. _php-8.1-resources-turned-into-objects:

PHP 8.1 Resources Turned Into Objects
+++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		PHP 8.1 Resources Turned Into Objects: Multiple PHP native functions now return objects, not resources.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 8.1 Resources Turned Into Objects
	:twitter:description: PHP 8.1 Resources Turned Into Objects: Multiple PHP native functions now return objects, not resources
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 8.1 Resources Turned Into Objects
	:og:type: article
	:og:description: Multiple PHP native functions now return objects, not resources
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/Php81RemovesResources.html
	:og:locale: en
Multiple PHP native functions now return objects, not resources. Any check on those values with `is_resource() <https://www.php.net/is_resource>`_ is now going to fail.

The affected functions are the following : 

+ `finfo_open() <https://www.php.net/finfo_open>`_
+ `ftp_connect() <https://www.php.net/ftp_connect>`_
+ `imap_open() <https://www.php.net/imap_open>`_
+ `ldap_connect() <https://www.php.net/ldap_connect>`_
+ `ldap_list() <https://www.php.net/ldap_list>`_
+ `ldap_search() <https://www.php.net/ldap_search>`_
+ `ldap_first_entry() <https://www.php.net/ldap_first_entry>`_
+ ldap_next_entry ()
+ `ldap_read() <https://www.php.net/ldap_read>`_
+ `pg_connect() <https://www.php.net/pg_connect>`_
+ `pg_pconnect() <https://www.php.net/pg_pconnect>`_
+ `pg_query() <https://www.php.net/pg_query>`_
+ pg_execute ()
+ `pg_lo_create() <https://www.php.net/pg_lo_create>`_
+ `pspell_config_create() <https://www.php.net/pspell_config_create>`_
+ `pspell_new() <https://www.php.net/pspell_new>`_
+ `pspell_new_personal() <https://www.php.net/pspell_new_personal>`_
+ `pspell_new_config() <https://www.php.net/pspell_new_config>`_

 

.. code-block:: php
   
   <?php
   
   $pspell = new pspell_new(en, , , ,
                        (PSPELL_FAST|PSPELL_RUN_TOGETHER));
   var_dump(is_resource($pspell)); // true in PHP 8.0, 
   							    // false in PHP 8.1
   
   ?>

See also `UPGRADING PHP 8.1 <https://www.php.net/manual/en/migration81.incompatible.php#migration81.incompatible.resource2object>`_.

Connex PHP features
-------------------

  + `resource <https://php-dictionary.readthedocs.io/en/latest/dictionary/resource.ini.html>`_


Suggestions
___________

* Change the condition from is_resource() to instanceof




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/Php81RemovesResources                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.2.0                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.1                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


