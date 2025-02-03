.. _php-oldautoloadusage:

.. _old-style-\_\_autoload():

Old Style __autoload()
++++++++++++++++++++++

.. meta::
	:description:
		Old Style __autoload(): Avoid __autoload(), only use spl_register_autoload().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Old Style __autoload()
	:twitter:description: Old Style __autoload(): Avoid __autoload(), only use spl_register_autoload()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Old Style __autoload()
	:og:type: article
	:og:description: Avoid __autoload(), only use spl_register_autoload()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Old Style __autoload().html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/oldAutoloadUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/oldAutoloadUsage.html","name":"Old Style __autoload()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Avoid __autoload(), only use spl_register_autoload()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Old Style __autoload().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Avoid __autoload(), only use spl_register_autoload().

__autoload() is deprecated since PHP 7.2 and possibly removed in later versions. spl_register_autoload() was introduced in PHP 5.1.0.

__autoload() may only be declared once, and cannot be modified later. This creates potential conflicts between libraries that try to set up their own autoloading schema. 

On the other hand, spl_register_autoload() allows registering and unregistering multiple autoloading functions or methods. 

Do not use the old __autoload() function, but rather the new spl_register_autoload() function.

.. code-block:: php
   
   <?php
   
   // Modern autoloading.
   function myAutoload($class){}
   spl_register_autoload('myAutoload');
   
   // Old style autoloading.
   function __autoload($class){}
   
   ?>

See also `Autoloading Classes <https://www.php.net/manual/en/language.oop5.autoload.php>`_.

Related PHP errors 
-------------------

  + `__autoload() is deprecated, use spl_autoload_register() instead <https://php-errors.readthedocs.io/en/latest/messages/__autoload%28%29-is-deprecated%2C-use-spl_autoload_register%28%29-instead.html>`_
  + `__autoload() is no longer supported, use spl_autoload_register() instead <https://php-errors.readthedocs.io/en/latest/messages/__autoload%28%29-is-no-longer-supported%2C-use-spl_autoload_register%28%29-instead.html>`_



Connex PHP features
-------------------

  + `autoload <https://php-dictionary.readthedocs.io/en/latest/dictionary/autoload.ini.html>`_


Suggestions
___________

* Move to spl_register_autoload()
* Remove usage of the old __autoload() function
* Modernize usage of old libraries




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/oldAutoloadUsage                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `use-smart-autoload <https://github.com/dseguy/clearPHP/tree/master/rules/use-smart-autoload.md>`__                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-piwigo-php-oldautoloadusage`                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


