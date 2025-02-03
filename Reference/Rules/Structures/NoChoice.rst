.. _structures-nochoice:


.. _no-choice:

No Choice
+++++++++


.. meta::

	:description:

		No Choice: A conditional structure is being used, and both alternatives are the same, leading to the illusion of choice.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: No Choice

	:twitter:description: No Choice: A conditional structure is being used, and both alternatives are the same, leading to the illusion of choice

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: No Choice

	:og:type: article

	:og:description: A conditional structure is being used, and both alternatives are the same, leading to the illusion of choice

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Choice.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoChoice.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoChoice.html","name":"No Choice","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"A conditional structure is being used, and both alternatives are the same, leading to the illusion of choice","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Choice.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A conditional structure is being used, and both alternatives are the same, leading to the illusion of choice. 

Either the condition is useless, and may be removed, or the alternatives need to be distinguished.

.. code-block:: php
   
   <?php
   
   if ($condition == 2) {
       doSomething();
   } else {
       doSomething();
   }
   
   $condition == 2 ?     doSomething() :     doSomething();
   
   ?>
Connex PHP features
-------------------

  + `branch <https://php-dictionary.readthedocs.io/en/latest/dictionary/branch.ini.html>`_
  + `condition <https://php-dictionary.readthedocs.io/en/latest/dictionary/condition.ini.html>`_


Suggestions
___________

* Remove the conditional, and call the expression directly
* Replace one of the alternative with a distinct call
* Remove the whole conditional : it may end up being useless
* Extract the common elements of the condition to make them obvious




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoChoice                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Rector <ruleset-Rector>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-nextcloud-structures-nochoice`, :ref:`case-zencart-structures-nochoice`                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


