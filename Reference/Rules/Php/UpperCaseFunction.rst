.. _php-uppercasefunction:


.. _unusual-case-for-php-functions:

Unusual Case For PHP Functions
++++++++++++++++++++++++++++++


.. meta::

	:description:

		Unusual Case For PHP Functions: Usually, PHP functions are written all in lower case.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Unusual Case For PHP Functions

	:twitter:description: Unusual Case For PHP Functions: Usually, PHP functions are written all in lower case

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Unusual Case For PHP Functions

	:og:type: article

	:og:description: Usually, PHP functions are written all in lower case

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unusual Case For PHP Functions.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UpperCaseFunction.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UpperCaseFunction.html","name":"Unusual Case For PHP Functions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"Usually, PHP functions are written all in lower case","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unusual Case For PHP Functions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Usually, PHP functions are written all in lower case. There might a reason for the writing in uppercase, so it is recommended to investigate, and revert to the usual convention.

.. code-block:: php
   
   <?php
   
   // All uppercases PHP functions
   ECHO STRTOLOWER('This String');
   
   ?>
Connex PHP features
-------------------

  + `function <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `coding-convention <https://php-dictionary.readthedocs.io/en/latest/dictionary/coding-convention.ini.html>`_


Suggestions
___________

* Use the PHP casing for functions




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UpperCaseFunction                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


