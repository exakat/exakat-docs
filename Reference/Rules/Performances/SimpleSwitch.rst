.. _performances-simpleswitch:


.. _simple-switch-and-match:

Simple Switch And Match
+++++++++++++++++++++++

.. meta::
	:description:
		Simple Switch And Match: Switch() and match() are faster when relying only on literal integers or strings.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Simple Switch And Match
	:twitter:description: Simple Switch And Match: Switch() and match() are faster when relying only on literal integers or strings
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Simple Switch And Match
	:og:type: article
	:og:description: Switch() and match() are faster when relying only on literal integers or strings
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Simple Switch And Match.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/SimpleSwitch.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/SimpleSwitch.html","name":"Simple Switch And Match","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Switch() and match() are faster when relying only on literal integers or strings","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Simple Switch And Match.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`Switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ and `match() <https://www.php.net/manual/en/control-structures.match.php>`_ are faster when relying only on literal integers or strings.

Since PHP 7.2, simple switches, that use only literal strings or integers, are optimized. The bigger the switch, the greater the gain.
`Match() <https://www.php.net/manual/en/control-structures.match.php>`_ was introduced in PHP 8.0

In particular, this optimisation doesn't work with any expressions (constant or not), function call, methodcall, constant usage, etc. Only literal values, string or integer.

When the switch is partially build of literals, it is worth splitting the switch in two : first level, only with the literal cases, and, in the default, the dynamic values. This brings some performances, though it is a micro-optimisation.

.. code-block:: php
   
   <?php
   
   // Optimized switch. 
   switch($b) {
       case "a":
           break;
       case "b":
           break;
       case "c":
           break;
       case "d":
           break;
       default :
           break;
   }
   
   // Unoptimized switch. 
   // Try moving the foo() call in the default, to keep the rest of the switch optimized.
   switch($c) {
       case "a":
           break;
       case foo($b):
           break;
       case C:
           break;
       case "c":
           break;
       case "d":
           break;
       default :
           break;
   }
   
   // Partially optimised switch
   // Try moving the foo() call in the default, to keep the rest of the switch optimized.
   switch($c) {
       case "a":
           break;
       case "c":
           break;
       case "d":
           break;
       default :
           switch($c) {
               case foo($b):
               break;
   
               case C:
               break;
   
           default :
               break;
           }
           break;
   }
   
   ?>

See also `PHP 7.2's "switch" optimisations <https://derickrethans.nl/php7.2-switch.html>`_.

Connex PHP features
-------------------

  + `switch <https://php-dictionary.readthedocs.io/en/latest/dictionary/switch.ini.html>`_
  + `match <https://php-dictionary.readthedocs.io/en/latest/dictionary/match.ini.html>`_


Suggestions
___________

* Split the switch between literal and dynamic cases
* Remove the dynamic cases from the switch
* Move the most common case to the beginning of the switch




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/SimpleSwitch                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.1                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.2 and more recent                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


