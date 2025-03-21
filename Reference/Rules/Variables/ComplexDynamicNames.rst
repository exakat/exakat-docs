.. _variables-complexdynamicnames:


.. _complex-dynamic-names:

Complex Dynamic Names
+++++++++++++++++++++

.. meta::
	:description:
		Complex Dynamic Names: Avoid using expressions as names for variables or methods.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Complex Dynamic Names
	:twitter:description: Complex Dynamic Names: Avoid using expressions as names for variables or methods
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Complex Dynamic Names
	:og:type: article
	:og:description: Avoid using expressions as names for variables or methods
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Complex Dynamic Names.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/ComplexDynamicNames.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/ComplexDynamicNames.html","name":"Complex Dynamic Names","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Avoid using expressions as names for variables or methods","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Complex Dynamic Names.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid using expressions as names for variables or methods. 

There are no place for checks or flow control, leading to any rogue value to be used as is. Besides, the expression is often overlooked, and not expected there : this makes the code less readable.

It is recommended to build the name in a separate variable, apply the usual checks for existence and validity, and then use the name.
This analysis only accept simple containers, such as variables, properties.

.. code-block:: php
   
   <?php
   
   $a = new foo();
   
   // Code is more readable
   $name = strolower($string);
   if (!property_exists($a, $name)) {
       throw new missingPropertyexception($name);
   }
   echo $a->$name;
   
   // This is not check
   echo $a->{strtolower($string)};
   
   ?>

See also  `Dynamically Access PHP Object Properties with $this <https://drupalize.me/blog/201508/dynamically-access-php-object-properties>`_.

Connex PHP features
-------------------

  + `Dynamic Variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-variable.ini.html>`_


Suggestions
___________

* Extract the expression from the variable syntax, and make it a separate variable.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/ComplexDynamicNames                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.4                                                                                                                   |
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


