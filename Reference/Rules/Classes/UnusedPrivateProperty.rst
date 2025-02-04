.. _classes-unusedprivateproperty:


.. _unused-private-properties:

Unused Private Properties
+++++++++++++++++++++++++

.. meta::
	:description:
		Unused Private Properties: Unused static properties should be removed.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Private Properties
	:twitter:description: Unused Private Properties: Unused static properties should be removed
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Private Properties
	:og:type: article
	:og:description: Unused static properties should be removed
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unused Private Properties.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UnusedPrivateProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UnusedPrivateProperty.html","name":"Unused Private Properties","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Unused static properties should be removed","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unused Private Properties.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Unused `static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties should be removed. 

Unused private properties are dead code. They are usually leftovers of development or refactorisation : they used to have a mission, but are now left. 

Being private, those properties are only accessible to the current class or trait. As such, validating the

.. code-block:: php
   
   <?php
   
   class foo {
       // This is a used property (see bar method)
       private $used = 1;
   
       // This is an unused property
       private $unused = 2;
       
       function bar($a) {
           $this->used += $a;
           
           return $this->used;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `Unused <https://php-dictionary.readthedocs.io/en/latest/dictionary/unused.ini.html>`_


Suggestions
___________

* Remove the property altogether
* Check if the property wasn't forgotten in the rest of the class
* Check if the property is correctly named
* Change the visibility to protected or public : may be a visibility refactoring was too harsh




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnusedPrivateProperty                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Dead code <ruleset-Dead-code>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openemr-classes-unusedprivateproperty`, :ref:`case-phpadsnew-classes-unusedprivateproperty`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


