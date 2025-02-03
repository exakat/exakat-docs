.. _extensions-extintl:

.. _ext-intl:

ext/intl
++++++++

.. meta::
	:description:
		ext/intl: Extension international.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/intl
	:twitter:description: ext/intl: Extension international
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/intl
	:og:type: article
	:og:description: Extension international
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/intl.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extintl.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extintl.html","name":"ext\/intl","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension international","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/intl.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Extension international.

Internationalization extension (further is referred as Intl) is a wrapper for `ICU <http://site.icu-project.org/>`_ library, enabling PHP programmers to perform various `locale <https://www.php.net/locale>`_-aware operations including but not limited to formatting, transliteration, encoding conversion, calendar operations, `UCA <http://www.unicode.org/reports/tr10/>`_-conformant collation, locating text boundaries and working with `locale <https://www.php.net/locale>`_ identifiers, timezones and graphemes.

.. code-block:: php
   
   <?php
   $coll = new Collator('en_US');
   $al   = $coll->getLocale(Locale::ACTUAL_LOCALE);
   echo "Actual locale: $al\n";
   
   $formatter = new NumberFormatter('en_US', NumberFormatter::DECIMAL);
   echo $formatter->format(1234567);
   ?>

See also `Internationalization Functions <https://www.php.net/manual/en/book.intl.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extintl                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


