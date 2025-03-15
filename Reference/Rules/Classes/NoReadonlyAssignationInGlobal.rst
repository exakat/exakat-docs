.. _classes-noreadonlyassignationinglobal:


.. _no-readonly-assignation-in-global:

No Readonly Assignation In Global
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		No Readonly Assignation In Global: When a property is marked readonly, it may only be assigned within the class of definition.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Readonly Assignation In Global
	:twitter:description: No Readonly Assignation In Global: When a property is marked readonly, it may only be assigned within the class of definition
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Readonly Assignation In Global
	:og:type: article
	:og:description: When a property is marked readonly, it may only be assigned within the class of definition
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Readonly Assignation In Global.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NoReadonlyAssignationInGlobal.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NoReadonlyAssignationInGlobal.html","name":"No Readonly Assignation In Global","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"When a property is marked readonly, it may only be assigned within the class of definition","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Readonly Assignation In Global.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When a property is marked readonly, it may only be assigned within the class of definition.

It cannot be assigned outside this class, in the global scope. It is also immune to class invasion.

.. code-block:: php
   
   <?php
   
   class x {
       public readonly int $p;
       
       function foo() {
           $this->p -= 1; // OK
           
           $x = new x;
           $x->p = 1;     // Not OK, even if $x is of type x
       }
   }
   
   $x = new x;
   $x->p = 1;     // Not OK
   
   ?>
Related PHP errors 
-------------------

  + `Cannot initialize readonly property %s::$%s from global scope <https://php-errors.readthedocs.io/en/latest/messages/cannot-%25s-readonly-property-%25s%3A%3A%24%25s-from-%25s%25s.html>`_
  + `Cannot initialize readonly property %s::$%s from scope %s <https://php-errors.readthedocs.io/en/latest/messages/cannot-%25s-readonly-property-%25s%3A%3A%24%25s-from-%25s%25s.html>`_



Connex PHP features
-------------------

  + `Readonly <https://php-dictionary.readthedocs.io/en/latest/dictionary/readonly.ini.html>`_
  + `Class Invasion <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-invasion.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NoReadonlyAssignationInGlobal                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


