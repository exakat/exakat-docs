.. _structures-yodacomparison:


.. _yoda-comparison:

Yoda Comparison
+++++++++++++++


.. meta::

	:description:

		Yoda Comparison: Yoda comparison is a way to write conditions which places literal values on the left side.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Yoda Comparison

	:twitter:description: Yoda Comparison: Yoda comparison is a way to write conditions which places literal values on the left side

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Yoda Comparison

	:og:type: article

	:og:description: Yoda comparison is a way to write conditions which places literal values on the left side

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Yoda Comparison.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/YodaComparison.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/YodaComparison.html","name":"Yoda Comparison","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 28 Jan 2025 15:14:39 +0000","dateModified":"Tue, 28 Jan 2025 15:14:39 +0000","description":"Yoda comparison is a way to write conditions which places literal values on the left side","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Yoda Comparison.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Yoda comparison is a way to write conditions which places literal values on the left side. 

The objective is to avoid mistaking a comparison to an assignation. If the comparison operator is mistaken, but the literal is on the left, then an `error <https://www.php.net/error>`_ will be triggered, instead of a silent bug.

Yoda comparison are not used when they are considered more confusing than helping.

.. code-block:: php
   
   <?php
   
   if (1 == $a) {
       // Then condition
   }
   
   ?>

See also `Yoda Conditions <https://en.wikipedia.org/wiki/Yoda_conditions>`_ and `Yoda Conditions: To Yoda or Not to Yoda <https://knowthecode.io/yoda-conditions-yoda-not-yoda>`_.

Connex PHP features
-------------------

  + `coding-convention <https://php-dictionary.readthedocs.io/en/latest/dictionary/coding-convention.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/YodaComparison                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


