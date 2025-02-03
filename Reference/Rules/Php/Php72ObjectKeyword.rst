.. _php-php72objectkeyword:


.. _php-7.2-object-keyword:

PHP 7.2 Object Keyword
++++++++++++++++++++++


.. meta::

	:description:

		PHP 7.2 Object Keyword: 'object' is a PHP keyword.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: PHP 7.2 Object Keyword

	:twitter:description: PHP 7.2 Object Keyword: 'object' is a PHP keyword

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: PHP 7.2 Object Keyword

	:og:type: article

	:og:description: 'object' is a PHP keyword

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP 7.2 Object Keyword.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php72ObjectKeyword.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php72ObjectKeyword.html","name":"PHP 7.2 Object Keyword","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"'object' is a PHP keyword","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP 7.2 Object Keyword.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

'object' is a PHP keyword. It can't be used for class, interface or trait name. 

This is the case since PHP 7.2.

.. code-block:: php
   
   <?php
   
   // Valid until PHP 7.2
   class object {}
   
   // Altough it is really weird anyway...
   
   ?>

See also `List of Keywords <https://www.php.net/manual/en/reserved.keywords.php>`_.


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php72ObjectKeyword                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.2 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


