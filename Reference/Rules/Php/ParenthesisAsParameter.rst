.. _php-parenthesisasparameter:


.. _parenthesis-as-parameter:

Parenthesis As Parameter
++++++++++++++++++++++++

.. meta::
	:description:
		Parenthesis As Parameter: Using parenthesis around parameters used to silent some internal check.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Parenthesis As Parameter
	:twitter:description: Parenthesis As Parameter: Using parenthesis around parameters used to silent some internal check
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Parenthesis As Parameter
	:og:type: article
	:og:description: Using parenthesis around parameters used to silent some internal check
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Parenthesis As Parameter.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ParenthesisAsParameter.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ParenthesisAsParameter.html","name":"Parenthesis As Parameter","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"Using parenthesis around parameters used to silent some internal check","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Parenthesis As Parameter.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Using parenthesis around parameters used to silent some internal check. This is not the case anymore in PHP 7, and should be fixed by removing the parenthesis and making the value a real reference.

.. code-block:: php
   
   <?php
   // example extracted from the PHP manual
   function getArray() {
       return [1, 2, 3];
   }
   
   function squareArray(array &$a) {
       foreach ($a as &$v) {
           $v \*\*\= 2;
       }
   }
   
   // Generates a warning in PHP 7.
   squareArray((getArray()));
   ?>

See also `Parentheses around function arguments no longer affect behaviour <https://www.php.net/manual/en/migration70.incompatible.php#migration70.incompatible.variable-handling.parentheses>`_.

Related PHP errors 
-------------------

  + `Only variables should be passed by reference <https://php-errors.readthedocs.io/en/latest/messages/only-variables-should-be-passed-by-reference.html>`_



Connex PHP features
-------------------

  + `Parenthesis <https://php-dictionary.readthedocs.io/en/latest/dictionary/parenthesis.ini.html>`_
  + `Parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/parameter.ini.html>`_


Suggestions
___________

* Remove the parenthesis when they are only encapsulating an argument
* Replace the parenthesis by the no-scream operator




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ParenthesisAsParameter                                                                                                                                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                                                                                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


