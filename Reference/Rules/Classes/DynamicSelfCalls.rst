.. _classes-dynamicselfcalls:

.. _dynamic-self-calls:

Dynamic Self Calls
++++++++++++++++++

.. meta::
	:description:
		Dynamic Self Calls: A class that calls itself dynamically.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dynamic Self Calls
	:twitter:description: Dynamic Self Calls: A class that calls itself dynamically
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dynamic Self Calls
	:og:type: article
	:og:description: A class that calls itself dynamically
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dynamic Self Calls.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DynamicSelfCalls.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DynamicSelfCalls.html","name":"Dynamic Self Calls","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"A class that calls itself dynamically","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Dynamic Self Calls.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>A class that calls itself dynamically. This may be property or methods. 

Calling itself dynamically happens when a class is configured to call various properties (container) or methods.  
This rule is mostly useful internally, to side some special situations.

.. code-block:: php
   
   <?php
   
   class x {
       function foo() {
           $f = 'goo';
           return $this->$f();
       }
   
       function goo() {
           return rand(1, 10);
       }
   }
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DynamicSelfCalls                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


