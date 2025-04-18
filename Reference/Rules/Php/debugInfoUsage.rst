.. _php-debuginfousage:


.. _\_\_debuginfo()-usage:

__debugInfo() Usage
+++++++++++++++++++

.. meta::
	:description:
		__debugInfo() Usage: The magic method __debugInfo() provides a custom way to dump an object.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: __debugInfo() Usage
	:twitter:description: __debugInfo() Usage: The magic method __debugInfo() provides a custom way to dump an object
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: __debugInfo() Usage
	:og:type: article
	:og:description: The magic method __debugInfo() provides a custom way to dump an object
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/__debugInfo() Usage.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/debugInfoUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/debugInfoUsage.html","name":"__debugInfo() Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The magic method __debugInfo() provides a custom way to dump an object","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/__debugInfo() Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The magic method `__debugInfo() <https://www.php.net/manual/en/language.oop5.magic.php>`_ provides a custom way to dump an object. 

It has been introduced in PHP 5.6. In the previous versions of PHP, this method is ignored and won't be called when debugging.

.. code-block:: php
   
   <?php
   
   // PHP 5.6 or later
   class foo {
       private $bar = 1;
       private $reallyHidden = 2;
       
       function __debugInfo() {
           return ['bar' => $this->bar,
                   'reallyHidden' => 'Secret'];
       }
   }
   
   $f = new Foo();
   var_dump($f);
   
   /* Displays : 
   object(foo)#1 (2) {
     [bar]=>
     int(1)
     [reallyHidden]=>
     string(6) Secret
   }
   */
   
   ?>

See also `Magic methods <https://www.php.net/manual/en/language.oop5.magic.php>`_.

Connex PHP features
-------------------

  + `Magic Methods <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/debugInfoUsage                                                                                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.6 and more recent                                                                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolibarr-php-debuginfousage`                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


