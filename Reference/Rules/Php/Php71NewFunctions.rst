.. _php-php71newfunctions:

.. _new-functions-in-php-7.1:

New Functions In PHP 7.1
++++++++++++++++++++++++

.. meta::
	:description:
		New Functions In PHP 7.1: The following functions are now native functions in PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: New Functions In PHP 7.1
	:twitter:description: New Functions In PHP 7.1: The following functions are now native functions in PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: New Functions In PHP 7.1
	:og:type: article
	:og:description: The following functions are now native functions in PHP 7
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/New Functions In PHP 7.1.html
	:og:locale: en
The following functions are now native functions in PHP 7.1. It is advised to change them before moving to this new version.

* `curl_share_strerror() <https://www.php.net/curl_share_strerror>`_
* `curl_multi_errno() <https://www.php.net/curl_multi_errno>`_
* `curl_share_errno() <https://www.php.net/curl_share_errno>`_
* `mb_ord() <https://www.php.net/mb_ord>`_
* `mb_chr() <https://www.php.net/mb_chr>`_
* `mb_scrub() <https://www.php.net/mb_scrub>`_
* `is_iterable() <https://www.php.net/is_iterable>`_
Connex PHP features
-------------------

  + `function <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `native <https://php-dictionary.readthedocs.io/en/latest/dictionary/native.ini.html>`_


Suggestions
___________

* Remove usage of the mentioned functions
* Use a polyfill to recreate the feature without relying on the function




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php71NewFunctions                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.1 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


