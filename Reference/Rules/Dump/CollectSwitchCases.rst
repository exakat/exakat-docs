.. _dump-collectswitchcases:


.. _collect-switch-cases-count:

Collect Switch Cases Count
++++++++++++++++++++++++++

.. meta::
	:description:
		Collect Switch Cases Count: This rule counts the number of cases in a switch or a match structure.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Switch Cases Count
	:twitter:description: Collect Switch Cases Count: This rule counts the number of cases in a switch or a match structure
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Switch Cases Count
	:og:type: article
	:og:description: This rule counts the number of cases in a switch or a match structure
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Collect Switch Cases Count.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectSwitchCases.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectSwitchCases.html","name":"Collect Switch Cases Count","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 02 May 2025 17:39:47 +0000","dateModified":"Fri, 02 May 2025 17:39:47 +0000","description":"This rule counts the number of cases in a switch or a match structure","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Collect Switch Cases Count.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule counts the number of cases in a switch or a match structure. Cases and default are both counted.

.. code-block:: php
   
   <?php
   
   // A switch with 4 cases: 3 cases + the default
   switch($a) {
       case 1:
       case 2:
       case 3:
       default:
   }
   
   ?>
Connex PHP features
-------------------

  + `Switch <https://php-dictionary.readthedocs.io/en/latest/dictionary/switch.ini.html>`_
  + `Default <https://php-dictionary.readthedocs.io/en/latest/dictionary/default.ini.html>`_
  + `Match <https://php-dictionary.readthedocs.io/en/latest/dictionary/match.ini.html>`_
  + `Case <https://php-dictionary.readthedocs.io/en/latest/dictionary/case.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------+
| Short name   | Dump/CollectSwitchCases                              |
+--------------+------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Dump <ruleset-Dump>` |
+--------------+------------------------------------------------------+
| Exakat since | 2.7.2                                                |
+--------------+------------------------------------------------------+
| PHP Version  | All                                                  |
+--------------+------------------------------------------------------+
| Severity     | Minor                                                |
+--------------+------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                      |
+--------------+------------------------------------------------------+
| Precision    | Very high                                            |
+--------------+------------------------------------------------------+
| Available in |                                                      |
+--------------+------------------------------------------------------+


