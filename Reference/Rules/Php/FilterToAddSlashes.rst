.. _php-filtertoaddslashes:

.. _filter-to-add\_slashes():

Filter To add_slashes()
+++++++++++++++++++++++

.. meta::
	:description:
		Filter To add_slashes(): ``FILTER_SANITIZE_MAGIC_QUOTES`` is deprecated.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Filter To add_slashes()
	:twitter:description: Filter To add_slashes(): ``FILTER_SANITIZE_MAGIC_QUOTES`` is deprecated
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Filter To add_slashes()
	:og:type: article
	:og:description: ``FILTER_SANITIZE_MAGIC_QUOTES`` is deprecated
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Filter To add_slashes().html
	:og:locale: en
``FILTER_SANITIZE_MAGIC_QUOTES`` is deprecated. In PHP 7.4, it should be replaced with `addslashes() <https://www.php.net/addslashes>`_

According to the migration RDFC : 'Magic quotes were deprecated all the way back in PHP 5.3 and later removed in PHP 5.4. The filter extension implements a sanitization filter that mimics this behavior of magic_quotes by calling `addslashes() <https://www.php.net/addslashes>`_ on the input in question.'
`addslashes() <https://www.php.net/addslashes>`_ used to filter data while building SQL queries, to prevent injections. Nowadays, prepared queries are a better option.

.. code-block:: php
   
   <?php
   
   // Deprecated way to filter input
   $var = filter_input($input, FILTER_SANITIZE_MAGIC_QUOTES);
   
   // Alternative way to filter input
   $var = addslashes($input);
   
   ?>

See also `Deprecations for PHP 7.4 <https://wiki.php.net/rfc/deprecations_php_7_4>`_.


Suggestions
___________

* Replace ``FILTER_SANITIZE_MAGIC_QUOTES`` with addslashes()
* Replace ``FILTER_SANITIZE_MAGIC_QUOTES`` with an adapted escaping system




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/FilterToAddSlashes                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


