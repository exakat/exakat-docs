.. _type-sapi:


.. _php-sapi:

PHP Sapi
++++++++

.. meta::
	:description:
		PHP Sapi: List of PHP SAPI mentioned in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP Sapi
	:twitter:description: PHP Sapi: List of PHP SAPI mentioned in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP Sapi
	:og:type: article
	:og:description: List of PHP SAPI mentioned in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP Sapi.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Sapi.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Sapi.html","name":"PHP Sapi","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"List of PHP SAPI mentioned in the code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP Sapi.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

List of PHP SAPI mentioned in the code. When those SAPI are mentioned in strings, they are usually checked to take advantage of special characteristics. Check the code for portability.

.. code-block:: php
   
   <?php
   
   require __DIR__.'/phpdbg.php';
   
   $Phpdbg = new phpdbg();
   
   ?>

See also `php_sapi_name() <https://www.php.net/manual/en/function.php-sapi-name.php>`_.

Connex PHP features
-------------------

  + `Server Application Programming Interface (SAPI) <https://php-dictionary.readthedocs.io/en/latest/dictionary/sapi.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/Sapi                                                                                                               |
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


