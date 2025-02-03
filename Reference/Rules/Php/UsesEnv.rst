.. _php-usesenv:

.. _uses-environment:

Uses Environment
++++++++++++++++

.. meta::
	:description:
		Uses Environment: This rule spots usage of ``$_ENV``, ``getenv()`` and ``putenv()`` functions: they fetch data from the environment variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Uses Environment
	:twitter:description: Uses Environment: This rule spots usage of ``$_ENV``, ``getenv()`` and ``putenv()`` functions: they fetch data from the environment variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Uses Environment
	:og:type: article
	:og:description: This rule spots usage of ``$_ENV``, ``getenv()`` and ``putenv()`` functions: they fetch data from the environment variables
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Uses Environment.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UsesEnv.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UsesEnv.html","name":"Uses Environment","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This rule spots usage of ``$_ENV``, ``getenv()`` and ``putenv()`` functions: they fetch data from the environment variables","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Uses Environment.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This rule spots usage of ``$_ENV``, ``getenv()`` and ``putenv()`` functions: they fetch data from the environment variables.

.. code-block:: php
   
   <?php
   
   // Take some configuration from the environment
   $secret_key = getenv('secret_key');
   
   ?>
Connex PHP features
-------------------

  + `system <https://php-dictionary.readthedocs.io/en/latest/dictionary/system.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UsesEnv                                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
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


