.. _namespaces-overloadexistingnames:


.. _overload-existing-names:

Overload Existing Names
+++++++++++++++++++++++

.. meta::
	:description:
		Overload Existing Names: Imported alias have precedence over existing ones, and as such, may replace existing features with unexpected ones.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Overload Existing Names
	:twitter:description: Overload Existing Names: Imported alias have precedence over existing ones, and as such, may replace existing features with unexpected ones
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Overload Existing Names
	:og:type: article
	:og:description: Imported alias have precedence over existing ones, and as such, may replace existing features with unexpected ones
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Overload Existing Names.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/OverloadExistingNames.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/OverloadExistingNames.html","name":"Overload Existing Names","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Imported alias have precedence over existing ones, and as such, may replace existing features with unexpected ones","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Overload Existing Names.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Imported alias have precedence over existing ones, and as such, may replace existing features with unexpected ones. 

This example shows how to replace `strtolower() <https://www.php.net/strtolower>`_ with `strtoupper() <https://www.php.net/strtoupper>`_ while keeping the main code intact. This might be very confusing code. 
This behavior is important for backward compatibility, and also to avoid naming conflicts when the coding has been done with a PHP installation which do not have some specific declaration. For example, a source may define an 'Event' class, which will be in conflict when the ext/event library is installed. 

This feature is also useful to mock some native PHP structures, during tests. 

This rule relies on the PDFF configuration to check for external existing structures.

.. code-block:: php
   
   <?php
   
   // Replacing a PHP classic with another one
   use function strtoupper as strtolower;
   
   echo strtolower('pHp'); 
   // displays PHP
   
   ?>
Connex PHP features
-------------------

  + `use-alias <https://php-dictionary.readthedocs.io/en/latest/dictionary/use-alias.ini.html>`_


Suggestions
___________

* Use another local name than the general name
* Always code in a namespace to avoid conflict




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/OverloadExistingNames                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


