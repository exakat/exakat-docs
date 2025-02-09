.. _structures-wronglocale:


.. _wrong-locale:

Wrong Locale
++++++++++++

.. meta::
	:description:
		Wrong Locale: This rule checks the locale used in the code, against a library of known valid locales.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong Locale
	:twitter:description: Wrong Locale: This rule checks the locale used in the code, against a library of known valid locales
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong Locale
	:og:type: article
	:og:description: This rule checks the locale used in the code, against a library of known valid locales
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Locale.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/WrongLocale.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/WrongLocale.html","name":"Wrong Locale","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This rule checks the locale used in the code, against a library of known valid locales","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Wrong Locale.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule checks the `locale <https://www.php.net/locale>`_ used in the code, against a library of known valid locales. Unknown locales are reported: they might be typos or unknown to certain systems.

.. code-block:: php
   
   <?php
   
   // what language ? 
   setLocale(LC_ALL, 'hx');
   
   // utf8 actually needs a - : utf-8
   setLocale(LC_ALL, 'utf8');
   
   ?>

+--------------+---------+---------+------------------------------------------------+
| Name         | Default | Type    | Description                                    |
+--------------+---------+---------+------------------------------------------------+
| otherLocales |         | array   | Other accepted locales, comma separated        |
+--------------+---------+---------+------------------------------------------------+
| maxPositions | 3       | integer | Number of argument in setLocale() to be tried. |
+--------------+---------+---------+------------------------------------------------+


Connex PHP features
-------------------

  + `Locale <https://php-dictionary.readthedocs.io/en/latest/dictionary/locale.ini.html>`_


Suggestions
___________

* Use a valid locale




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/WrongLocale                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


