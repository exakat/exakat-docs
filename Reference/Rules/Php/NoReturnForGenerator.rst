.. _php-noreturnforgenerator:

.. _no-return-for-generator:

No Return For Generator
+++++++++++++++++++++++

.. meta::
	:description:
		No Return For Generator: Return is not allowed in a generator function.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Return For Generator
	:twitter:description: No Return For Generator: Return is not allowed in a generator function
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Return For Generator
	:og:type: article
	:og:description: Return is not allowed in a generator function
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Return For Generator.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NoReturnForGenerator.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NoReturnForGenerator.html","name":"No Return For Generator","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 14 Jan 2025 12:52:58 +0000","dateModified":"Tue, 14 Jan 2025 12:52:58 +0000","description":"Return is not allowed in a generator function","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Return For Generator.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Return is not allowed in a `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_ function. In PHP versions 5.5 and 5.6, they yield a fatal `Error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   function generatorWithReturn() {
       yield 1;
       return 2;
   }
   
   ?>

See also `Generators overview <https://www.php.net/manual/en/language.generators.overview.php>`_.

Related PHP errors 
-------------------

  + `Generators cannot return values using "return" <https://php-errors.readthedocs.io/en/latest/messages/generators-cannot-return-values-using-%22return%22.html>`_



Connex PHP features
-------------------

  + `generator <https://php-dictionary.readthedocs.io/en/latest/dictionary/generator.ini.html>`_
  + `yield <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield.ini.html>`_


Suggestions
___________

* Remove usage of return in the generator
* Update PHP to version 7.0 or later




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NoReturnForGenerator                                                                                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.9                                                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


