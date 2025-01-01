.. _php-php72newconstants:

.. _new-constants-in-php-7.2:

New Constants In PHP 7.2
++++++++++++++++++++++++

.. meta::
	:description:
		New Constants In PHP 7.2: The following constants are now native in PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: New Constants In PHP 7.2
	:twitter:description: New Constants In PHP 7.2: The following constants are now native in PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: New Constants In PHP 7.2
	:og:type: article
	:og:description: The following constants are now native in PHP 7
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/Php72NewConstants.html
	:og:locale: en
The following constants are now native in PHP 7.2. It is advised to avoid using such names for constant before moving to this new version.

* ``PHP_OS_FAMILY``
* ``PHP_FLOAT_DIG``
* ``PHP_FLOAT_EPSILON``
* ``PHP_FLOAT_MAX``
* ``PHP_FLOAT_MIN``
* ``SQLITE3_DETERMINISTIC``
* ``CURLSSLOPT_NO_REVOKE``
* ``CURLOPT_DEFAULT_PROTOCOL``
* ``CURLOPT_STREAM_WEIGHT``
* ``CURLMOPT_PUSHFUNCTION``
* ``CURL_PUSH_OK``
* ``CURL_PUSH_DENY``
* ``CURL_HTTP_VERSION_2TLS``
* ``CURLOPT_TFTP_NO_OPTIONS``
* ``CURL_HTTP_VERSION_2_PRIOR_KNOWLEDGE``
* ``CURLOPT_CONNECT_TO``
* ``CURLOPT_TCP_FASTOPEN``
* ``DNS_CAA``

See also `New global constants in 7.2 <https://www.php.net/manual/en/migration72.constants.php>`_.

Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Move the constants to a new namespace
* Remove the old constants
* Rename the old constants




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php72NewConstants                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.7                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.2 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


