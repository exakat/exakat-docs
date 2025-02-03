.. _functions-variableparameterambiguityinarrowfunction:


.. _variable-parameter-ambiguity-in-arrow-function:

Variable Parameter Ambiguity In Arrow Function
++++++++++++++++++++++++++++++++++++++++++++++


.. meta::

	:description:

		Variable Parameter Ambiguity In Arrow Function: Avoid using a parameter that is also the name of a local variable.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Variable Parameter Ambiguity In Arrow Function

	:twitter:description: Variable Parameter Ambiguity In Arrow Function: Avoid using a parameter that is also the name of a local variable

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Variable Parameter Ambiguity In Arrow Function

	:og:type: article

	:og:description: Avoid using a parameter that is also the name of a local variable

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Variable Parameter Ambiguity In Arrow Function.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/VariableParameterAmbiguityInArrowFunction.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/VariableParameterAmbiguityInArrowFunction.html","name":"Variable Parameter Ambiguity In Arrow Function","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Avoid using a parameter that is also the name of a local variable","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Variable Parameter Ambiguity In Arrow Function.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid using a parameter that is also the name of a local variable.

Arrow functions import automatically the variables from the local context in their body. Yet, a variable name may also be used as the name of a parameter. In that case, PHP use the parameter, and omits the value of the local variable.

.. code-block:: php
   
   <?php
   
   // $b is a parameter, $a is a local variable
   $a = 1;
   fn($b) => $a + $b;
   
   //  $a is a local variable, but also a parameter.
   // PHP uses the parameter, and omits the local variable
   fn($a) => $a + 1;
   
   ?>
Connex PHP features
-------------------

  + `arrow-function <https://php-dictionary.readthedocs.io/en/latest/dictionary/arrow-function.ini.html>`_


Suggestions
___________

* Use parameter names that are distinct from the local variables names.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/VariableParameterAmbiguityInArrowFunction                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


