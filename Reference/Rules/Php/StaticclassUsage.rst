.. _php-staticclassusage:


.. _class:

\:\:class
+++++++++

.. meta::
	:description:
		::class: PHP has a special class constant to hold the name of the class : ``class`` keyword.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ::class
	:twitter:description: ::class: PHP has a special class constant to hold the name of the class : ``class`` keyword
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ::class
	:og:type: article
	:og:description: PHP has a special class constant to hold the name of the class : ``class`` keyword
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/::class.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/StaticclassUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/StaticclassUsage.html","name":"::class","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP has a special class constant to hold the name of the class : ``class`` keyword","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/::class.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP has a special class constant to hold the name of the class : ``class`` keyword. It represents the class name that is used in the left part of the operator.

Using ``\:\:class`` is safer than relying on a string. It does adapt if the class's name or its namespace is changed'. It is also faster, though it is a micro-optimisation. 

It is introduced in PHP 5.5.
Be aware that ``\:\:class`` is a replacement for `__CLASS__ <https://www.php.net/manual/en/language.constants.predefined.php>`_ magic constant.

.. code-block:: php
   
   <?php
   
   use A\B\C as UsedName;
   
   class foo {
       public function bar( ) {
           echo ClassName::class; 
           echo UsedName::class; 
       }
   }
   
   $f = new Foo( );
   $f->bar( );
   // displays ClassName 
   // displays A\B\C 
   
   ?>

See also `Class Constant <https://www.php.net/manual/en/language.oop5.constants.php>`_.

Connex PHP features
-------------------

  + `coalesce <https://php-dictionary.readthedocs.io/en/latest/dictionary/coalesce.ini.html>`_


Suggestions
___________

* Use ::class whenever possible. That exclude any dynamic call.




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/StaticclassUsage                                                                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.5 and more recent                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


