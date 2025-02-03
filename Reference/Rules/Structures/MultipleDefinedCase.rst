.. _structures-multipledefinedcase:


.. _multiples-identical-case:

Multiples Identical Case
++++++++++++++++++++++++


.. meta::

	:description:

		Multiples Identical Case: Some cases are defined multiple times, but only one will be processed.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Multiples Identical Case

	:twitter:description: Multiples Identical Case: Some cases are defined multiple times, but only one will be processed

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Multiples Identical Case

	:og:type: article

	:og:description: Some cases are defined multiple times, but only one will be processed

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Multiples Identical Case.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MultipleDefinedCase.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MultipleDefinedCase.html","name":"Multiples Identical Case","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Some cases are defined multiple times, but only one will be processed","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Multiples Identical Case.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Some cases are defined multiple times, but only one will be processed. Check the list of cases, and remove the extra one.

Exakat finds the value of the cases as much as possible, and ignore any dynamic cases (using variables).
It is also possible to write a valid switch statement, with all identical cases, and yet, different meaning each time. This is considered an edge case, and shall be manually removed.

.. code-block:: php
   
   <?php
   
   const A = 1;
   
   case ($x) {
       case 1 : 
           break;
       case true:    // This is a duplicate of the previous
           break; 
       case 1 + 0:   // This is a duplicate of the previous
           break; 
       case 1.0 :    // This is a duplicate of the previous
           break; 
       case A :      // The A constant is actually 1
           break; 
       case $y  :    // This is not reported.
           break; 
       default:
           
   }
   ?>
Connex PHP features
-------------------

  + `switch <https://php-dictionary.readthedocs.io/en/latest/dictionary/switch.ini.html>`_


Suggestions
___________

* Remove the double case
* Change the case to another and rightful value




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MultipleDefinedCase                                                                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Rector <ruleset-Rector>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-duplicate-case <https://github.com/dseguy/clearPHP/tree/master/rules/no-duplicate-case.md>`__                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-sugarcrm-structures-multipledefinedcase`, :ref:`case-expressionengine-structures-multipledefinedcase`                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


