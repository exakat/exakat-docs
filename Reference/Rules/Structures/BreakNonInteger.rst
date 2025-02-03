.. _structures-breaknoninteger:


.. _break-with-non-integer:

Break With Non Integer
++++++++++++++++++++++


.. meta::

	:description:

		Break With Non Integer: When using a break, the argument of the operator must be a positive non-null integer literal or be omitted.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Break With Non Integer

	:twitter:description: Break With Non Integer: When using a break, the argument of the operator must be a positive non-null integer literal or be omitted

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Break With Non Integer

	:og:type: article

	:og:description: When using a break, the argument of the operator must be a positive non-null integer literal or be omitted

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Break With Non Integer.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/BreakNonInteger.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/BreakNonInteger.html","name":"Break With Non Integer","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"When using a break, the argument of the operator must be a positive non-null integer literal or be omitted","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Break With Non Integer.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When using a `break <https://www.php.net/manual/en/control-structures.break.php>`_, the argument of the operator must be a positive non-null integer literal or be omitted.

Other values were acceptable in PHP 5.3 and previous version, but they are now reported as an `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
       // Can't break $a, even if it contains an integer.
       $a = 1;
       for($i = 0; $i < 10; $i++) {
           break $a;
       }
   
       // can't break on float
       for($i = 0; $i < 10; $i++) {
           for($j = 0; $j < 10; $j++) {
               break 2.2;
           }
       }
   
   ?>
Related PHP errors 
-------------------

  + `break operator accepts only positive integers <https://php-errors.readthedocs.io/en/latest/messages/break-operator-accepts-only-positive-integers.html>`_




Suggestions
___________

* Only use integer with break




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/BreakNonInteger                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.4 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


