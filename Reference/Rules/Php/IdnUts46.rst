.. _php-idnuts46:


.. _idn\_to\_ascii()-new-default:

idn_to_ascii() New Default
++++++++++++++++++++++++++


.. meta::

	:description:

		idn_to_ascii() New Default: The default parameter value of idn_to_ascii() and idn_to_utf8() is now `INTL_IDNA_VARIANT_UTS46` instead of the deprecated ``INTL_IDNA_VARIANT_2003``.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: idn_to_ascii() New Default

	:twitter:description: idn_to_ascii() New Default: The default parameter value of idn_to_ascii() and idn_to_utf8() is now `INTL_IDNA_VARIANT_UTS46` instead of the deprecated ``INTL_IDNA_VARIANT_2003``

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: idn_to_ascii() New Default

	:og:type: article

	:og:description: The default parameter value of idn_to_ascii() and idn_to_utf8() is now `INTL_IDNA_VARIANT_UTS46` instead of the deprecated ``INTL_IDNA_VARIANT_2003``

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/idn_to_ascii() New Default.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/IdnUts46.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/IdnUts46.html","name":"idn_to_ascii() New Default","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The default parameter value of idn_to_ascii() and idn_to_utf8() is now `INTL_IDNA_VARIANT_UTS46` instead of the deprecated ``INTL_IDNA_VARIANT_2003``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/idn_to_ascii() New Default.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The default parameter value of `idn_to_ascii() <https://www.php.net/idn_to_ascii>`_ and `idn_to_utf8() <https://www.php.net/idn_to_utf8>`_ is now `INTL_IDNA_VARIANT_UTS46` instead of the deprecated ``INTL_IDNA_VARIANT_2003``.

.. code-block:: php
   
   <?php
   
   echo idn_to_ascii('täst.de'); 
   
   ?>

See also `idn_to_ascii <https://www.php.net/manual/en/function.idn-to-ascii.php>`_, `idn_to_utf8 <https://www.php.net/manual/en/function.idn-to-utf8.php>`_ and `Unicode IDNA Compatibility Processing <http://unicode.org/reports/tr46/>`_.

Connex PHP features
-------------------

  + `internationalization <https://php-dictionary.readthedocs.io/en/latest/dictionary/internationalization.ini.html>`_


Suggestions
___________

* Explicitly add the second parameter to the idn_to_ascii() and idn_to_utf8() functions.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/IdnUts46                                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.3                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


