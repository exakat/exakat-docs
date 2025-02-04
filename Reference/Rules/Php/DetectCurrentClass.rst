.. _php-detectcurrentclass:


.. _detect-current-class:

Detect Current Class
++++++++++++++++++++

.. meta::
	:description:
		Detect Current Class: Detecting the current class should be done with `self::class` or `static::class` operator.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Detect Current Class
	:twitter:description: Detect Current Class: Detecting the current class should be done with `self::class` or `static::class` operator
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Detect Current Class
	:og:type: article
	:og:description: Detecting the current class should be done with `self::class` or `static::class` operator
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Detect Current Class.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/DetectCurrentClass.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/DetectCurrentClass.html","name":"Detect Current Class","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Detecting the current class should be done with `self::class` or `static::class` operator","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Detect Current Class.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Detecting the current class should be done with `self\:\:class` or `static\:\:class` operator.

`__CLASS__ <https://www.php.net/manual/en/language.constants.predefined.php>`_ may be replaced by ``self\:\:class``. 
`get_called_class() <https://www.php.net/get_called_class>`_ may be replaced by ``static\:\:class``. 

`__CLASS__ <https://www.php.net/manual/en/language.constants.predefined.php>`_ and `get_called_class() <https://www.php.net/get_called_class>`_ are set to be deprecated in PHP 7.4.

.. code-block:: php
   
   <?php
   
   class X {
       function foo() {
           echo __CLASS__."\n";          // X
           echo self::class."\n";        // X
           
           echo get_called_class()."\n";  // Y
           echo static::class."\n";       // Y
       }
   }
   
   class Y extends X {}
   
   $y = new Y();
   $y->foo();
   
   ?>

See also `PHP RFC: Deprecations for PHP 7.4 <https://wiki.php.net/rfc/deprecations_php_7_4>`_.

Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Use the self::class operator to detect the current class name, instead of __CLASS__ and get_class().
* Use the static::class operator to detect the current called class name, instead of get_called_class().




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/DetectCurrentClass                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.8                                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


