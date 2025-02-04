.. _classes-makeglobalaproperty:


.. _make-global-a-property:

Make Global A Property
++++++++++++++++++++++

.. meta::
	:description:
		Make Global A Property: Calling global (or $GLOBALS) in methods is slower and less testable than setting the global to a property, and using this property.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Make Global A Property
	:twitter:description: Make Global A Property: Calling global (or $GLOBALS) in methods is slower and less testable than setting the global to a property, and using this property
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Make Global A Property
	:og:type: article
	:og:description: Calling global (or $GLOBALS) in methods is slower and less testable than setting the global to a property, and using this property
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Make Global A Property.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MakeGlobalAProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MakeGlobalAProperty.html","name":"Make Global A Property","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Calling global (or $GLOBALS) in methods is slower and less testable than setting the global to a property, and using this property","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Make Global A Property.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Calling global (or $GLOBALS) in methods is slower and less testable than setting the global to a property, and using this property.

Using properties is slightly faster than calling global or $GLOBALS, though the gain is not important. 

Setting the property in the constructor (or in a factory), makes the class easier to test, as there is now a single point of configuration.

.. code-block:: php
   
   <?php 
   
   // Wrong way
   class fooBad {
       function x() {
           global $a;
           $a->do();
           // Or $GLOBALS['a']->do();
       }
   }
   
   class fooGood {
       private $bar = null;
       
       function __construct() {
           global $bar; 
           $this->bar = $bar;
           // Even better, do this via arguments
       }
       
       function x() {
           $this->a->do();
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `Global Variables <https://php-dictionary.readthedocs.io/en/latest/dictionary/global-variable.ini.html>`_


Suggestions
___________

* Avoid using global variables, and use properties instead
* Remove the usage of these global variables




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MakeGlobalAProperty                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


