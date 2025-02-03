.. _files-definitionsonly:


.. _definitions-only:

Definitions Only
++++++++++++++++

.. meta::
	:description:
		Definitions Only: File is definition only.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Definitions Only
	:twitter:description: Definitions Only: File is definition only
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Definitions Only
	:og:type: article
	:og:description: File is definition only
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Definitions Only.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Files\/DefinitionsOnly.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Files\/DefinitionsOnly.html","name":"Definitions Only","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"File is definition only","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Definitions Only.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

File is definition only.

Definition-only files only include structure definitions : class, functions, traits, interfaces, constants, global, declare(), use and include().

Some functioncalls are also considered definition only, as they configure PHP, but don't process data : 
* `ini_set() <https://www.php.net/ini_set>`_
* error_reporting
* `register_shutdown_function() <https://www.php.net/register_shutdown_function>`_
* set_session_handler()
* `set_error_handler() <https://www.php.net/set_error_handler>`_
* `spl_autoload_register() <https://www.php.net/spl_autoload_register>`_
File A : 
File B :

.. code-block:: php
   
   <?php
   
   // This file has only definitions
   function foo() {}
   
   define('a', 1);
   
   class bar {}
   
   ?>
Connex PHP features
-------------------

  + `definition <https://php-dictionary.readthedocs.io/en/latest/dictionary/definition.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Files/DefinitionsOnly                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


