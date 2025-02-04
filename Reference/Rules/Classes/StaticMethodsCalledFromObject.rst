.. _classes-staticmethodscalledfromobject:


.. _static-methods-called-from-object:

Static Methods Called From Object
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Static Methods Called From Object: Static methods may be called without instantiating an object.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Static Methods Called From Object
	:twitter:description: Static Methods Called From Object: Static methods may be called without instantiating an object
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Static Methods Called From Object
	:og:type: article
	:og:description: Static methods may be called without instantiating an object
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Static Methods Called From Object.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/StaticMethodsCalledFromObject.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/StaticMethodsCalledFromObject.html","name":"Static Methods Called From Object","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Static methods may be called without instantiating an object","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Static Methods Called From Object.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`Static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods may be called without instantiating an object. As such, they never interact with the special variable '`$this <https://www.php.net/manual/en/language.oop5.basic.php>`_', as they do not depend on object existence. 

Besides this, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods are normal methods that may be called directly from object context, to perform some utility task. 

To maintain code readability, it is recommended to call `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method in a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ way, rather than within object context.

.. code-block:: php
   
   <?php
       class x {
           static function y( ) {}
       }
       
       $z = new x( );
       
       $z->y( ); // Readability : no one knows it is a static call
       x::y( );  // Readability : here we know
   ?>
Connex PHP features
-------------------

  + `Object <https://php-dictionary.readthedocs.io/en/latest/dictionary/object.ini.html>`_
  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Suggestions
___________

* Switch to static method syntax
* Remove the static option from the method




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/StaticMethodsCalledFromObject                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


