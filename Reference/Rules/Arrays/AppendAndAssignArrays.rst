.. _arrays-appendandassignarrays:


.. _append-and-assign-arrays:

Append And Assign Arrays
++++++++++++++++++++++++


.. meta::

	:description:

		Append And Assign Arrays: This rule reports arrays that are used both with append and direct index assignation.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Append And Assign Arrays

	:twitter:description: Append And Assign Arrays: This rule reports arrays that are used both with append and direct index assignation

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Append And Assign Arrays

	:og:type: article

	:og:description: This rule reports arrays that are used both with append and direct index assignation

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Append And Assign Arrays.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/AppendAndAssignArrays.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/AppendAndAssignArrays.html","name":"Append And Assign Arrays","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"This rule reports arrays that are used both with append and direct index assignation","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Append And Assign Arrays.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports arrays that are used both with append and direct index assignation. Read access are not considered here. 

Array append and direct index assignation have different impact one on the other. In particular, assign a value explicitely and later append values may have an impact on one another.

.. code-block:: php
   
   <?php
   
   $arrayAppend = array();
   $arrayAppend[] = 1;
   
   ?>
Connex PHP features
-------------------

  + `append <https://php-dictionary.readthedocs.io/en/latest/dictionary/append.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/AppendAndAssignArrays                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


