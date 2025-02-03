.. _interfaces-alreadyparentsinterface:

.. _already-parents-interface:

Already Parents Interface
+++++++++++++++++++++++++

.. meta::
	:description:
		Already Parents Interface: The same interface is implemented by a class and one of its children.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Already Parents Interface
	:twitter:description: Already Parents Interface: The same interface is implemented by a class and one of its children
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Already Parents Interface
	:og:type: article
	:og:description: The same interface is implemented by a class and one of its children
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Already Parents Interface.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/AlreadyParentsInterface.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/AlreadyParentsInterface.html","name":"Already Parents Interface","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"The same interface is implemented by a class and one of its children","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Already Parents Interface.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The same interface is implemented by a class and one of its children. 

That way, the child doesn't need to implement the interface, nor define its methods to be an instance of the interface. 
This analysis may report classes which do not explicitly implements any interfaces : the issue is then coming from the parents.

.. code-block:: php
   
   <?php
   
   interface i { 
       function i();
   }
   
   class A implements i {
       function i() {
           return __METHOD__;
       }
   }
   
   // This implements is useless. 
   class AB extends A implements i {
       // No definition for function i()
   }
   
   // Implements i is understated
   class AB extends A {
       // redefinition of the i method
       function i() {
           return __METHOD__.' ';
       }
   }
   
   $x = new AB;
   var_dump($x instanceof i);
   // true
   
   $x = new AC;
   var_dump($x instanceof i);
   // true
   
   ?>
Connex PHP features
-------------------

  + `implements <https://php-dictionary.readthedocs.io/en/latest/dictionary/implements.ini.html>`_
  + `inheritance <https://php-dictionary.readthedocs.io/en/latest/dictionary/inheritance.ini.html>`_


Suggestions
___________

* Keep the implements call in the class that do implements the methods. Remove it from the children classes.




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/AlreadyParentsInterface                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-interfaces-alreadyparentsinterface`, :ref:`case-thelia-interfaces-alreadyparentsinterface`                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


