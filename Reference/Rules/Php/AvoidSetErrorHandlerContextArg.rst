.. _php-avoidseterrorhandlercontextarg:


.. _avoid-set\_error\_handler-$context-argument:

Avoid set_error_handler $context Argument
+++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Avoid set_error_handler $context Argument: Avoid configuring set_error_handler() with a method that accepts 5 arguments.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid set_error_handler $context Argument
	:twitter:description: Avoid set_error_handler $context Argument: Avoid configuring set_error_handler() with a method that accepts 5 arguments
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid set_error_handler $context Argument
	:og:type: article
	:og:description: Avoid configuring set_error_handler() with a method that accepts 5 arguments
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Avoid set_error_handler $context Argument.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/AvoidSetErrorHandlerContextArg.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/AvoidSetErrorHandlerContextArg.html","name":"Avoid set_error_handler $context Argument","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Avoid configuring set_error_handler() with a method that accepts 5 arguments","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Avoid set_error_handler $context Argument.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid configuring `set_error_handler() <https://www.php.net/set_error_handler>`_ with a method that accepts 5 arguments. The last argument, ``$errcontext``, is deprecated since PHP 7.2, and will be removed later.

.. code-block:: php
   
   <?php
   
   // setting error_handler with an incorrect closure
   set_error_handler(function($errno, $errstr, $errfile, $errline) {});
   
   // setting error_handler with an incorrect closure
   set_error_handler(function($errno, $errstr, $errfile, $errline, $errcontext) {});
   
   ?>

See also set_error_handler().

Connex PHP features
-------------------

  + `Error Handler <https://php-dictionary.readthedocs.io/en/latest/dictionary/error-handler.ini.html>`_


Suggestions
___________

* Remove the 6th argument of registered handlers.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/AvoidSetErrorHandlerContextArg                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-shopware-php-avoidseterrorhandlercontextarg`, :ref:`case-vanilla-php-avoidseterrorhandlercontextarg`                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


