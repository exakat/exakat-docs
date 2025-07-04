.. _classes-propertyneverused:


.. _never-used-properties:

Never Used Properties
+++++++++++++++++++++

.. meta::
	:description:
		Never Used Properties: Properties that are never used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Never Used Properties
	:twitter:description: Never Used Properties: Properties that are never used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Never Used Properties
	:og:type: article
	:og:description: Properties that are never used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Never Used Properties.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PropertyNeverUsed.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PropertyNeverUsed.html","name":"Never Used Properties","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Properties that are never used","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Never Used Properties.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Properties that are never used. They are defined in a class or a trait, but they never actually used.

Properties are considered used when they are used locally, in the same class as their definition, or in a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class : a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class is always included with the current class. 

On the other hand, properties which are defined in a class, but only used in children classes is considered unused, since children may also avoid using it.

.. code-block:: php
   
   <?php
   
   class foo {
       public $usedProperty = 1;
   
       // Never used anywhere
       public $unusedProperty = 2;
       
       function bar() {
           // Used internally
           ++$this->usedProperty;
       }
   }
   
   class foo2  extends foo {
       function bar2() {
           // Used in child class
           ++$this->usedProperty;
       }
   }
   
   // Used externally
   ++$this->usedProperty;
   
   ?>
Connex PHP features
-------------------

  + `Properties <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Suggestions
___________

* Drop unused properties
* Change the name of the unused properties
* Move the properties to children classes
* Find usage for unused properties




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PropertyNeverUsed                                                                                               |
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
| Examples     | :ref:`case-wordpress-classes-propertyneverused`                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


