.. _structures-calltimepassbyreference:


.. _calltime-pass-by-reference:

Calltime Pass By Reference
++++++++++++++++++++++++++

.. meta::
	:description:
		Calltime Pass By Reference: PHP doesn't allow when a value is turned into a reference at functioncall, since PHP 5.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Calltime Pass By Reference
	:twitter:description: Calltime Pass By Reference: PHP doesn't allow when a value is turned into a reference at functioncall, since PHP 5
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Calltime Pass By Reference
	:og:type: article
	:og:description: PHP doesn't allow when a value is turned into a reference at functioncall, since PHP 5
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Calltime Pass By Reference.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CalltimePassByReference.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CalltimePassByReference.html","name":"Calltime Pass By Reference","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"PHP doesn't allow when a value is turned into a reference at functioncall, since PHP 5","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Calltime Pass By Reference.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP doesn't allow when a value is turned into a reference at functioncall, since PHP 5.4. 

Either the function use a reference in its signature, either the reference won't pass.

.. code-block:: php
   
   <?php
   
   function foo($name) {
       $arg = ucfirst(strtolower($name));
       echo 'Hello '.$arg;
   }
   
   $a = 'name';
   foo(&$a);
   
   ?>

See also `Passing by Reference <https://www.php.net/manual/en/language.references.pass.php>`_.

Related PHP errors 
-------------------

  + `syntax error, unexpected token "&" <https://php-errors.readthedocs.io/en/latest/messages/syntax-error%2C-unexpected-token-%22%26%22.html>`_



Connex PHP features
-------------------

  + `Passing By Value <https://php-dictionary.readthedocs.io/en/latest/dictionary/by-value.ini.html>`_
  + `Passing By Reference <https://php-dictionary.readthedocs.io/en/latest/dictionary/by-reference.ini.html>`_


Suggestions
___________

* Make the signature of the called method accept references
* Remove the reference from the method call
* Use an object instead of a scalar




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CalltimePassByReference                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.4 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


