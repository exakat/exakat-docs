.. _variables-variablenonascii:


.. _non-ascii-variables:

Non Ascii Variables
+++++++++++++++++++

.. meta::
	:description:
		Non Ascii Variables: PHP allows certain characters in variable names.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Non Ascii Variables
	:twitter:description: Non Ascii Variables: PHP allows certain characters in variable names
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Non Ascii Variables
	:og:type: article
	:og:description: PHP allows certain characters in variable names
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Non Ascii Variables.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/VariableNonascii.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/VariableNonascii.html","name":"Non Ascii Variables","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP allows certain characters in variable names","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Non Ascii Variables.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP allows certain characters in variable names. The variable name must only include letters, figures, underscores and ASCII characters from 128 to 255. 

In practice, letters outside the scope of the intervalle ``[a-zA-Z0-9_]`` are rare, and require more care when editing the code or passing it from OS to OS. 

Also, certain letter might appear similar to the roman ones, and be part of a different alphabet. This is the case, for example, of the cyrillic alphabet, where `А` (cyrillic A, U+0410) is actually different from `A` (Latin A, U+0041). Some dashes and spaces may be valid in PHP variable names, and look very confusing.

.. code-block:: php
   
   <?php
   
   // person, in Simplified Chinese
   class 人 {
       // An actual working class in PHP.
       public function __construct() {
           echo __CLASS__;
       }
   }
   
   // people = new person();
   $人民 = new 人();
   
   ?>

See also `Variables <https://www.php.net/manual/en/language.variables.basics.php>`_.


Suggestions
___________

* Make sure those special chars have actual meaning.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/VariableNonascii                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-magento-variables-variablenonascii`                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


