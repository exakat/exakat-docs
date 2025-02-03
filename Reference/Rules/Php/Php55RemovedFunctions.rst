.. _php-php55removedfunctions:


.. _functions-removed-in-php-5.5:

Functions Removed In PHP 5.5
++++++++++++++++++++++++++++


.. meta::

	:description:

		Functions Removed In PHP 5.5: Those functions were removed in PHP 5.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Functions Removed In PHP 5.5

	:twitter:description: Functions Removed In PHP 5.5: Those functions were removed in PHP 5

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Functions Removed In PHP 5.5

	:og:type: article

	:og:description: Those functions were removed in PHP 5

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Functions Removed In PHP 5.5.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php55RemovedFunctions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php55RemovedFunctions.html","name":"Functions Removed In PHP 5.5","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Those functions were removed in PHP 5","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Functions Removed In PHP 5.5.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Those functions were removed in PHP 5.5.

+ `php_logo_guid() <https://www.php.net/php_logo_guid>`_
+ php_egg_logo_guid()
+ php_real_logo_guid()
+ `zend_logo_guid() <https://www.php.net/zend_logo_guid>`_
+ mcrypt_cbc()
+ mcrypt_cfb()
+ mcrypt_ecb()
+ mcrypt_ofb()

.. code-block:: php
   
   <?php
   
   echo '<img src="' . $_SERVER['PHP_SELF'] .
        '?=' . php_logo_guid() . '" alt="PHP Logo !" />';
   
   ?>

See also `Deprecated features in PHP 5.5.x <https://www.php.net/manual/en/migration55.deprecated.php>`_.

Connex PHP features
-------------------

  + `deprecated <https://php-dictionary.readthedocs.io/en/latest/dictionary/deprecated.ini.html>`_


Suggestions
___________

* Stop using those functions




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php55RemovedFunctions                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.5 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


