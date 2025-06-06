.. _structures-break0:


.. _break-with-0:

Break With 0
++++++++++++

.. meta::
	:description:
		Break With 0: It is not possible to break 0 : it makes no sense.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Break With 0
	:twitter:description: Break With 0: It is not possible to break 0 : it makes no sense
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Break With 0
	:og:type: article
	:og:description: It is not possible to break 0 : it makes no sense
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Break With 0.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/Break0.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/Break0.html","name":"Break With 0","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"It is not possible to break 0 : it makes no sense","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Break With 0.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

It is not possible to `break <https://www.php.net/manual/en/control-structures.break.php>`_ 0 : it makes no sense. `Break <https://www.php.net/manual/en/control-structures.break.php>`_ 1 is the minimum, and is the default value.

.. code-block:: php
   
   <?php
       // Can't break 0. Must be 1 or more, depending on the level of nesting.
       for($i = 0; $i < 10; $i++) {
           break 0;
       }
   
       for($i = 0; $i < 10; $i++) {
           for($j = 0; $j < 10; $j++) {
               break 2;
           }
       }
   
   ?>
Related PHP errors 
-------------------

  + `'break' operator accepts only positive integers <https://php-errors.readthedocs.io/en/latest/messages/%27%25s%27-operator-accepts-only-positive-integers.html>`_



Connex PHP features
-------------------

  + `Break <https://php-dictionary.readthedocs.io/en/latest/dictionary/break.ini.html>`_


Suggestions
___________

* Remove the operand 0
* Remove the break




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/Break0                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>` |
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


