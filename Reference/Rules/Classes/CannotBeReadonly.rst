.. _classes-cannotbereadonly:


.. _property-cannot-be-readonly:

Property Cannot Be Readonly
+++++++++++++++++++++++++++


.. meta::

	:description:

		Property Cannot Be Readonly: This analysis reports different situations where a property is readonly, and has some impossible code.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Property Cannot Be Readonly

	:twitter:description: Property Cannot Be Readonly: This analysis reports different situations where a property is readonly, and has some impossible code

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Property Cannot Be Readonly

	:og:type: article

	:og:description: This analysis reports different situations where a property is readonly, and has some impossible code

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Property Cannot Be Readonly.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CannotBeReadonly.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CannotBeReadonly.html","name":"Property Cannot Be Readonly","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This analysis reports different situations where a property is readonly, and has some impossible code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Property Cannot Be Readonly.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This analysis reports different situations where a property is readonly, and has some impossible code. 

Two cases are reported : 
+ a `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_-updated property, where it is updated with a value that is created from itself. The most obvious is ``$this->a = `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_->a;`` (which is reported as an `error <https://www.php.net/error>`_ by PHP), and ``$this->a = foo(`$this <https://www.php.net/manual/en/language.oop5.basic.php>`_->a);`` is the most common.
+ a property which is set in the constructor, yet has a distinct method where it is updated too. 

Most of thoses cases are dead code.

.. code-block:: php
   
   <?php
   
   class x {
   	private readonly $p;
   	private readonly $q;
   	
   	function __construct($p) {
   		$this->p = $p; // normal assignation
   	}
   	
   	function foo() {
   		$this->q = bar($this->q); // this is not possible with readonly
   		$this->q++; // this is not possible with readonly
   		$this->q[] = 2; // this is not possible with readonly
   	}
   }
   
   ?>
Connex PHP features
-------------------

  + `readonly <https://php-dictionary.readthedocs.io/en/latest/dictionary/readonly.ini.html>`_
  + `dead-code <https://php-dictionary.readthedocs.io/en/latest/dictionary/dead-code.ini.html>`_


Suggestions
___________

* Remove the impossible code




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CannotBeReadonly                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.1                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


