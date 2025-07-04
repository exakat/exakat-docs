.. _php-noreferenceforternary:


.. _no-reference-for-ternary:

No Reference For Ternary
++++++++++++++++++++++++

.. meta::
	:description:
		No Reference For Ternary: The ternary operator and the null coalescing operator are both expressions that only return values, and not a reference.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Reference For Ternary
	:twitter:description: No Reference For Ternary: The ternary operator and the null coalescing operator are both expressions that only return values, and not a reference
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Reference For Ternary
	:og:type: article
	:og:description: The ternary operator and the null coalescing operator are both expressions that only return values, and not a reference
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Reference For Ternary.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NoReferenceForTernary.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NoReferenceForTernary.html","name":"No Reference For Ternary","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The ternary operator and the null coalescing operator are both expressions that only return values, and not a reference","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Reference For Ternary.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The ternary operator and the `null <https://www.php.net/`null <https://www.php.net/null>`_>`_ coalescing operator are both expressions that only return values, and not a reference. 

This means that any provided reference will be turned into its value. While this is usually invisible, it will raise a warning when a reference is expected. This is the case with methods returning a reference. 

A PHP notice is generated when using a ternary operator or the `null <https://www.php.net/`null <https://www.php.net/null>`_>`_ coalesce operator : ``Only variable references should be returned by reference``. The notice is also emitted when returning objects. 

This applies to methods, functions and closures.

.. code-block:: php
   
   <?php
   
   // This works
   function &foo($a, $b) { 
       if ($a === 1) {
           return $b; 
       } else {
           return $a; 
       }
   }
   
   // This raises a warning, as the operator returns a value
   function &foo($a, $b) { return $a === 1 ? $b : $a; }
   
   ?>

See also `Null Coalescing Operator <https://www.php.net/manual/en/language.operators.comparison.php#language.operators.comparison.coalesce>`_ and `Ternary Operator <https://www.php.net/manual/en/language.operators.comparison.php#language.operators.comparison.ternary>`_.

Related PHP errors 
-------------------

  + `Only variable references should be returned by reference <https://php-errors.readthedocs.io/en/latest/messages/only-variable-references-should-be-returned-by-reference.html>`_



Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Drop the reference at assignation time
* Drop the reference in the argument definition
* Drop the reference in the function return definition




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NoReferenceForTernary                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.8                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpadsnew-php-noreferenceforternary`                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


