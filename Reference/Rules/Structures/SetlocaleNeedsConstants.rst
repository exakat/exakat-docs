.. _structures-setlocaleneedsconstants:


.. _setlocale()-uses-constants:

Setlocale() Uses Constants
++++++++++++++++++++++++++

.. meta::
	:description:
		Setlocale() Uses Constants: setlocale() don't use strings but constants.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Setlocale() Uses Constants
	:twitter:description: Setlocale() Uses Constants: setlocale() don't use strings but constants
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Setlocale() Uses Constants
	:og:type: article
	:og:description: setlocale() don't use strings but constants
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Setlocale() Uses Constants.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SetlocaleNeedsConstants.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SetlocaleNeedsConstants.html","name":"Setlocale() Uses Constants","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"setlocale() don't use strings but constants","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Setlocale() Uses Constants.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`setlocale() <https://www.php.net/setlocale>`_ don't use strings but constants. 

The first argument of `setlocale() <https://www.php.net/setlocale>`_ must be one of the valid constants, ``LC_ALL``, ``LC_COLLATE``, ``LC_CTYPE``, ``LC_MONETARY``, ``LC_NUMERIC``, ``LC_TIME, `LC_MESSAGES <https://www.php.net/LC_MESSAGES>`_``.
The PHP 5 usage of strings (same name as above, enclosed in ' or ") is not legit anymore in PHP 7 and later.

.. code-block:: php
   
   <?php
   
   // Use constantes for setlocale first argument
   setlocale(LC_ALL, 'nl_NL');
   setlocale(\LC_ALL, 'nl_NL');
   
   // Don't use string for setlocale first argument
   setlocale('LC_ALL', 'nl_NL');
   setlocale('LC_'.'ALL', 'nl_NL');
   
   ?>

See also `setlocale <https://www.php.net/setlocale>`_.


Suggestions
___________

* Use setlocale() constants




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SetlocaleNeedsConstants                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


