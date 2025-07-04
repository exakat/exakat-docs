.. _exceptions-uselesstry:


.. _useless-try:

Useless Try
+++++++++++

.. meta::
	:description:
		Useless Try: This rule reports useless ``try`` clause.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Try
	:twitter:description: Useless Try: This rule reports useless ``try`` clause
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Try
	:og:type: article
	:og:description: This rule reports useless ``try`` clause
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Try.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/UselessTry.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/UselessTry.html","name":"Useless Try","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:12:06 +0000","dateModified":"Wed, 05 Mar 2025 15:12:06 +0000","description":"This rule reports useless ``try`` clause","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless Try.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports useless ``try`` clause. A try clause is useless when no `exception <https://www.php.net/exception>`_ is emitted by the code in the block. 

The rule searches the called methods inside the ``try`` block, and spots any throw. 

At the moment, the search is limited to one level deep.

.. code-block:: php
   
   <?php
   
   try {
   	// Nothing is going to happen here
   	++$a;
   	foo();
   } catch (Exception $e) {
   
   }
   
   function foo() {
       // doSomething but not throw
   }
   
   ?>
Connex PHP features
-------------------

  + `Try-catch <https://php-dictionary.readthedocs.io/en/latest/dictionary/try.ini.html>`_


Suggestions
___________

* Remove the Try clause
* Add a throw among the different called methods




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/UselessTry                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


