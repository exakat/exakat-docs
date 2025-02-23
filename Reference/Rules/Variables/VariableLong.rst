.. _variables-variablelong:


.. _variables-with-long-names:

Variables With Long Names
+++++++++++++++++++++++++

.. meta::
	:description:
		Variables With Long Names: This analysis collects all variables with more than 20 characters longs.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Variables With Long Names
	:twitter:description: Variables With Long Names: This analysis collects all variables with more than 20 characters longs
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Variables With Long Names
	:og:type: article
	:og:description: This analysis collects all variables with more than 20 characters longs
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Variables With Long Names.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/VariableLong.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/VariableLong.html","name":"Variables With Long Names","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This analysis collects all variables with more than 20 characters longs","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Variables With Long Names.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This analysis collects all variables with more than 20 characters longs. This may be configured with the ``variableLength`` parameter.
PHP has not limitation on variable name size. While short name are often obscure, long names are usually better. Yet, there exists a limit to convenient variable name length.

.. code-block:: php
   
   <?php
   
   // Quite a long variable name
   $There_is nothing_wrong_with_long_variable_names_They_tend_to_be_rare_and_that_make_them_noteworthy = 1;
   
   ?>

+----------------+---------+---------+----------------------------------------------------------------+
| Name           | Default | Type    | Description                                                    |
+----------------+---------+---------+----------------------------------------------------------------+
| variableLength | 20      | integer | Minimum size of a long variable name, including the initial $. |
+----------------+---------+---------+----------------------------------------------------------------+



See also `Basics <https://www.php.net/manual/en/language.variables.basics.php>`_.


Suggestions
___________

* Try to use short variable names.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/VariableLong                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


