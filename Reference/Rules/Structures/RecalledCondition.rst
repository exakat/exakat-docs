.. _structures-recalledcondition:


.. _recalled-condition:

Recalled Condition
++++++++++++++++++

.. meta::
	:description:
		Recalled Condition: A recalled condition is a check that is made twice : once in the condition, then again in the body of the structure, to collect the actual value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Recalled Condition
	:twitter:description: Recalled Condition: A recalled condition is a check that is made twice : once in the condition, then again in the body of the structure, to collect the actual value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Recalled Condition
	:og:type: article
	:og:description: A recalled condition is a check that is made twice : once in the condition, then again in the body of the structure, to collect the actual value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Recalled Condition.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/RecalledCondition.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/RecalledCondition.html","name":"Recalled Condition","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A recalled condition is a check that is made twice : once in the condition, then again in the body of the structure, to collect the actual value","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Recalled Condition.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A recalled condition is a check that is made twice : once in the condition, then again in the body of the structure, to collect the actual value. 

Usually, the second call may be skipped by storing the value in a local variable. à

The second call may be necessary when the call is not idempotent.

This is a speed optimisation: when the call is a simple property fetch, or include a local cache, it is a micro-optimisation. Otherwise, it has a good performance potential.

One of the option is to use an iffectation: an affectation in the condition. This serves as cache too. Otherwise, the condition may be calculated and stored before the condition.

.. code-block:: php
   
   <?php
   
   if (get('a')) {
   	$a = get('a');
   	echo "Here is a : $a\n";
   }
   
   ?>
Connex PHP features
-------------------

  + `Micro-optimisation <https://php-dictionary.readthedocs.io/en/latest/dictionary/micro-optimisation.ini.html>`_
  + `Idempotent <https://php-dictionary.readthedocs.io/en/latest/dictionary/idempotent.ini.html>`_
  + `Iffectation <https://php-dictionary.readthedocs.io/en/latest/dictionary/iffectation.ini.html>`_


Suggestions
___________

* Put the result of the call in a variable to cache it.
* Use an iffectation in the condition, both store the result and use it in the condition.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/RecalledCondition                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


