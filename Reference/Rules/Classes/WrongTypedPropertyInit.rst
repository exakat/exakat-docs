.. _classes-wrongtypedpropertyinit:


.. _wrong-typed-property-default:

Wrong Typed Property Default
++++++++++++++++++++++++++++


.. meta::

	:description:

		Wrong Typed Property Default: Property is typed, yet receives an incompatible value at constructor time.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Wrong Typed Property Default

	:twitter:description: Wrong Typed Property Default: Property is typed, yet receives an incompatible value at constructor time

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Wrong Typed Property Default

	:og:type: article

	:og:description: Property is typed, yet receives an incompatible value at constructor time

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Typed Property Default.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/WrongTypedPropertyInit.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/WrongTypedPropertyInit.html","name":"Wrong Typed Property Default","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"Property is typed, yet receives an incompatible value at constructor time","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Wrong Typed Property Default.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Property is typed, yet receives an incompatible value at constructor time.

Initialized type might be a new instance, the return of a method call or an interface compatible object.

PHP compiles such code, but won't execute it, as it detects the incompatibility at execution time.

.. code-block:: php
   
   <?php
   
   class X {
       private A $property;
       private B $incompatible;
       
       function __construct() {
           // This is compatible
           $this->property = new A();
           
           // This is incompatible : new B() expected
           $this->incompatible = new C();
           
       }
   }
   
   ?>

See also :ref:`Wrong Type Returned <wrong-type-returned>` and :ref:`Mismatch Type And Default <mismatch-type-and-default>`.

Related PHP errors 
-------------------

  + `Cannot use int as default value for parameter %s of type %s <https://php-errors.readthedocs.io/en/latest/messages/cannot-use-%25s-as-default-value-for-parameter-%24%25s-of-type-%25s.html>`_
  + `Cannot use int as default value for property %s::$%s of type %s <https://php-errors.readthedocs.io/en/latest/messages/cannot-use-%25s-as-default-value-for-property-%25s%3A%3A%24%25s-of-type-%25s.html>`_



Connex PHP features
-------------------

  + `default-value <https://php-dictionary.readthedocs.io/en/latest/dictionary/default-value.ini.html>`_


Suggestions
___________

* Remove the type hint of the property
* Fix the initialization call
* Use an interface for typehint




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/WrongTypedPropertyInit                                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.9                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and more recent                                                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


