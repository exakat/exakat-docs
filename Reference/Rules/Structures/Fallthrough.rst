.. _structures-fallthrough:


.. _switch-fallthrough:

Switch Fallthrough
++++++++++++++++++

.. meta::
	:description:
		Switch Fallthrough: A switch with fallthrough is prone to errors.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Switch Fallthrough
	:twitter:description: Switch Fallthrough: A switch with fallthrough is prone to errors
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Switch Fallthrough
	:og:type: article
	:og:description: A switch with fallthrough is prone to errors
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Switch Fallthrough.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/Fallthrough.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/Fallthrough.html","name":"Switch Fallthrough","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A switch with fallthrough is prone to errors","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Switch Fallthrough.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A switch with fallthrough is prone to errors. 

A fallthrough happens when a case or default clause in a switch statement is not finished by a `break <https://www.php.net/manual/en/control-structures.break.php>`_ (or equivalent);
CWE report this as a security concern, unless well documented.

A fallthrough may be used as a feature. Then, it is indistinguishable from an `error <https://www.php.net/error>`_. 

When the case block is empty, this analysis doesn't report it : the case is then used as an alias.
This analysis doesn't take into account comments about the fallthrough.

.. code-block:: php
   
   <?php
   switch($variable) {
       case 1 :   // case 1 is not reported, as it actually shares the same body as case 33
       case 33 :  
           break ;
       case 2 : 
           break ;
       default: 
           ++$a;
       case 4 : 
           break ;
   }
   ?>

See also `CWE-484: Omitted Break Statement in Switch <https://cwe.mitre.org/data/definitions/484.html>`_ and `Rule: no-switch-case-fall-through <https://palantir.github.io/tslint/rules/no-switch-case-fall-through/>`_.

Connex PHP features
-------------------

  + `Switch <https://php-dictionary.readthedocs.io/en/latest/dictionary/switch.ini.html>`_
  + `Switch Fallthrough <https://php-dictionary.readthedocs.io/en/latest/dictionary/fallthrough.ini.html>`_


Suggestions
___________

* Make separate code for each case. Always use break at the end of a case or default.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/Fallthrough                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`, :ref:`Security <ruleset-Security>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.14                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+


