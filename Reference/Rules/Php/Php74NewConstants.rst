.. _php-php74newconstants:


.. _new-constants-in-php-7.4:

New Constants In PHP 7.4
++++++++++++++++++++++++

.. meta::
	:description:
		New Constants In PHP 7.4: The following constants are now native in PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: New Constants In PHP 7.4
	:twitter:description: New Constants In PHP 7.4: The following constants are now native in PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: New Constants In PHP 7.4
	:og:type: article
	:og:description: The following constants are now native in PHP 7
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/New Constants In PHP 7.4.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php74NewConstants.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php74NewConstants.html","name":"New Constants In PHP 7.4","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The following constants are now native in PHP 7","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/New Constants In PHP 7.4.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The following constants are now native in PHP 7.4. It is advised to avoid using such names for constant before moving to this new version.

* ``MB_ONIGURUMA_VERSION``
* ``SO_LABEL``
* ``SO_PEERLABEL``
* ``SO_LISTENQLIMIT``
* ``SO_LISTENQLEN``
* ``SO_USER_COOKIE``
* ``PHP_WINDOWS_EVENT_CTRL_C``
* ``PHP_WINDOWS_EVENT_CTRL_BREAK``
* ``TIDY_TAG_ARTICLE``
* ``TIDY_TAG_ASIDE``
* ``TIDY_TAG_AUDIO``
* ``TIDY_TAG_BDI``
* ``TIDY_TAG_CANVAS``
* ``TIDY_TAG_COMMAND``
* ``TIDY_TAG_DATALIST``
* ``TIDY_TAG_DETAILS``
* ``TIDY_TAG_DIALOG``
* ``TIDY_TAG_FIGCAPTION``
* ``TIDY_TAG_FIGURE``
* ``TIDY_TAG_FOOTER``
* ``TIDY_TAG_HEADER``
* ``TIDY_TAG_HGROUP``
* ``TIDY_TAG_MAIN``
* ``TIDY_TAG_MARK``
* ``TIDY_TAG_MENUITEM``
* ``TIDY_TAG_METER``
* ``TIDY_TAG_NAV``
* ``TIDY_TAG_OUTPUT``
* ``TIDY_TAG_PROGRESS``
* ``TIDY_TAG_SECTION``
* ``TIDY_TAG_SOURCE``
* ``TIDY_TAG_SUMMARY``
* ``TIDY_TAG_TEMPLATE``
* ``TIDY_TAG_TIME``
* ``TIDY_TAG_TRACK``
* ``TIDY_TAG_VIDEO``
* ``STREAM_CRYPTO_METHOD_TLSv1_3_CLIENT``
* ``STREAM_CRYPTO_METHOD_TLSv1_3_SERVER``
* ``STREAM_CRYPTO_PROTO_TLSv1_3``
* ``T_COALESCE_EQUAL``
* ``T_FN``

See also `New global constants in 7.4 <https://www.php.net/manual/en/migration74.constants.php>`_.

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

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php74NewConstants                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


