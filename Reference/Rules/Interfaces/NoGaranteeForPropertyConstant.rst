.. _interfaces-nogaranteeforpropertyconstant:

.. _interfaces-don't-ensure-properties:

Interfaces Don't Ensure Properties
++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Interfaces Don't Ensure Properties: When using an interface as a type, properties are not enforced.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Interfaces Don't Ensure Properties
	:twitter:description: Interfaces Don't Ensure Properties: When using an interface as a type, properties are not enforced
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Interfaces Don't Ensure Properties
	:og:type: article
	:og:description: When using an interface as a type, properties are not enforced
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Interfaces Don't Ensure Properties.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/NoGaranteeForPropertyConstant.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/NoGaranteeForPropertyConstant.html","name":"Interfaces Don't Ensure Properties","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When using an interface as a type, properties are not enforced","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Interfaces Don't Ensure Properties.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>When using an interface as a type, properties are not enforced. They might be not available, and lead to a Fatal `Error <https://www.php.net/error>`_.

An interface is a template for a class, which specify the minimum amount of methods and constants. Properties are never defined in an interface, and should not be relied upon.

Properties may be defined in an abstract class. 


.. code-block:: php
   
   <?php
   
   interface i {
       function m () ;
   }
   
   class x implements i {
       public $p = 1;
       
       function m() {
           return $this->p;
       }
   }
   
   function foo(i $i, x $x) {
       // this is invalid, as $p is not defined in i, so it may be not available
       echo $i->p;
       
       // this is valid, as $p is defined in $x
       echo $x->p;
   }
   
   ?>

See also `Interface And Abstract Class <https://medium.com/@atakde/interface-and-abstract-class-6f5cae27fa07>`_.

Connex PHP features
-------------------

  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Suggestions
___________

* Use classes for type when properties are accessed
* Only use methods and constants which are available in the interface
* Use an abstract class




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/NoGaranteeForPropertyConstant                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.5                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


