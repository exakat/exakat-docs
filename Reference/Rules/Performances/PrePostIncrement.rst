.. _performances-prepostincrement:


.. _pre-increment:

Pre-increment
+++++++++++++


.. meta::

	:description:

		Pre-increment: When possible, use the pre-increment operator (``++$i`` or ``--$i``) instead of the post-increment operator (``$i++`` or ``$i--``).

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Pre-increment

	:twitter:description: Pre-increment: When possible, use the pre-increment operator (``++$i`` or ``--$i``) instead of the post-increment operator (``$i++`` or ``$i--``)

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Pre-increment

	:og:type: article

	:og:description: When possible, use the pre-increment operator (``++$i`` or ``--$i``) instead of the post-increment operator (``$i++`` or ``$i--``)

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Pre-increment.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/PrePostIncrement.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/PrePostIncrement.html","name":"Pre-increment","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When possible, use the pre-increment operator (``++$i`` or ``--$i``) instead of the post-increment operator (``$i++`` or ``$i--``)","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Pre-increment.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When possible, use the pre-increment operator (``++$i`` or ``--$i``) instead of the post-increment operator (``$i++`` or ``$i--``).

The latter needs an extra memory allocation that costs about 10% of performances. 
This is a micro-optimisation. However, its usage is so widespread, including within loops, that it may eventually have an significant impact on execution time. As such, it is recommended to adopt this rule, and only consider changing legacy code as they are refactored for other reasons.

.. code-block:: php
   
   <?php
   
   // ++$i should be preferred over $i++, as current value is not important
   for($i = 0; $i <10; ++$i) {
       // do Something
   }
   
   // ++$b and $b++ have different impact here, since $a will collect $b + 1 or $b, respectively.
   $a = $b++;
   
   ?>
Connex PHP features
-------------------

  + `increment <https://php-dictionary.readthedocs.io/en/latest/dictionary/increment.ini.html>`_


Suggestions
___________

* Use the pre increment when the new value is not reused.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/PrePostIncrement                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-expressionengine-performances-prepostincrement`, :ref:`case-traq-performances-prepostincrement`                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


