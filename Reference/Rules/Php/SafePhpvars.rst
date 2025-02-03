.. _php-safephpvars:


.. _safe-phpvariables:

Safe Phpvariables
+++++++++++++++++

.. meta::
	:description:
		Safe Phpvariables: Mark the safe PHP variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Safe Phpvariables
	:twitter:description: Safe Phpvariables: Mark the safe PHP variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Safe Phpvariables
	:og:type: article
	:og:description: Mark the safe PHP variables
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Safe Phpvariables.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/SafePhpvars.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/SafePhpvars.html","name":"Safe Phpvariables","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Mark the safe PHP variables","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Safe Phpvariables.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Mark the safe PHP variables. 

PHP superglobals are usually filled with external data that should be filtered. However, some values may be considered safe, as they are under the control of the developer.

``$_GET``, ``$_POST``, ``$_FILES``, ``$_REQUEST``, ``$_COOKIES`` are all considered unsafe. Their level of validation is checked in other analysis. 

``$_SERVER`` is partially safe. It is valid for the following values : ``DOCUMENT_ROOT``, ``REQUEST_TIME``, ``REQUEST_TIME_FLOAT``, ``SCRIPT_NAME``, ``SERVER_ADMIN``, ``_``.

.. code-block:: php
   
   <?php
   
   // DOCUMENT_ROOT is a safe variable
   echo $_SERVER['DOCUMENT_ROOT'];
   
   // $_SERVER's PHP_SELF MUST be validated before usage
   echo $_SERVER['PHP_SELF'];
   
   // $_GET MUST be validated before usage
   echo $_GET['_'];
   
   ?>

See also `Predefined Variables <https://www.php.net/manual/en/reserved.variables.php>`_.

Connex PHP features
-------------------

  + `superglobal <https://php-dictionary.readthedocs.io/en/latest/dictionary/superglobal.ini.html>`_
  + `php-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/php-variable.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/SafePhpvars                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


