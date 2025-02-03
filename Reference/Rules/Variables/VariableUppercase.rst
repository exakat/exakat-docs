.. _variables-variableuppercase:

.. _all-uppercase-variables:

All Uppercase Variables
+++++++++++++++++++++++

.. meta::
	:description:
		All Uppercase Variables: Usually, global variables are all in uppercase, so as to differentiate them easily.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: All Uppercase Variables
	:twitter:description: All Uppercase Variables: Usually, global variables are all in uppercase, so as to differentiate them easily
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: All Uppercase Variables
	:og:type: article
	:og:description: Usually, global variables are all in uppercase, so as to differentiate them easily
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/All Uppercase Variables.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/VariableUppercase.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/VariableUppercase.html","name":"All Uppercase Variables","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Usually, global variables are all in uppercase, so as to differentiate them easily","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/All Uppercase Variables.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Usually, global variables are all in uppercase, so as to differentiate them easily. Though, this is not always the case, with examples like $argc, $argv or $http_response_header.

When using custom variables, try to use lowercase ``$variables``, ``$camelCase``, ``$sturdyCase`` or ``$snake_case``.

.. code-block:: php
   
   <?php
   
   // PHP super global, also identified by the initial _
   $localVariable = $_POST;
   
   // PHP globals
   $localVariable = $GLOBALS['HTTPS'];
   
   ?>

See also `Predefined Variables <https://www.php.net/manual/en/reserved.variables.php>`_.

Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/VariableUppercase                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


