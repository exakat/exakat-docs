.. _classes-undefinedparentmp:


.. _undefined-parent:

Undefined Parent
++++++++++++++++

.. meta::
	:description:
		Undefined Parent: List of properties and methods that are accessed using ``parent`` keyword but are not defined in the parent classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Undefined Parent
	:twitter:description: Undefined Parent: List of properties and methods that are accessed using ``parent`` keyword but are not defined in the parent classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Undefined Parent
	:og:type: article
	:og:description: List of properties and methods that are accessed using ``parent`` keyword but are not defined in the parent classes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Undefined Parent.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UndefinedParentMP.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UndefinedParentMP.html","name":"Undefined Parent","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"List of properties and methods that are accessed using ``parent`` keyword but are not defined in the parent classes","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Undefined Parent.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

List of properties and methods that are accessed using ``parent`` keyword but are not defined in the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ classes. 

This may compile but, eventually yields a fatal `error <https://www.php.net/error>`_ during execution.

Note that if the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ is defined using ``extends someClass`` but ``someClass`` is not available in the tested code, it will not be reported : it may be in composer, another dependency, or just missing.

.. code-block:: php
   
   <?php
   
   class theParent {
       // No bar() method
       // private bar() method is not accessible to theChild 
   }
   
   class theChild extends theParent {
       function foo() {
           // bar is defined in theChild, but not theParent
           parent::bar();
       }
       
       function bar() {
       
       }
   }
   
   ?>

See also https://www.php.net/manual/en/keyword.parent.php.

Related PHP errors 
-------------------

  + `Call to undefined method %s::%s() <https://php-errors.readthedocs.io/en/latest/messages/call-to-undefined-method-%25s%3A%3A%25s%28%29.html>`_
  + `Cannot access parent:: when current class scope has no parent <https://php-errors.readthedocs.io/en/latest/messages/cannot-access-parent%3A%3A-when-current-class-scope-has-no-parent.html>`_



Connex PHP features
-------------------

  + `parent <https://php-dictionary.readthedocs.io/en/latest/dictionary/parent.ini.html>`_


Suggestions
___________

* Remove the usage of the found method
* Add a definition for the method in the appropriate parent
* Fix the name of the method, and replace it with a valid definition
* Change 'parent' with 'self' if the method is eventually defined in the current class
* Change 'parent' with another object, if the method has been defined in another class
* Add the 'extends' keyword to the class, to actually have a parent class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UndefinedParentMP                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


