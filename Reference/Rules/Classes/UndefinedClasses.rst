.. _classes-undefinedclasses:


.. _undefined-classes:

Undefined Classes
+++++++++++++++++

.. meta::
	:description:
		Undefined Classes: Those classes are used in the code, but there are no definition for them.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Undefined Classes
	:twitter:description: Undefined Classes: Those classes are used in the code, but there are no definition for them
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Undefined Classes
	:og:type: article
	:og:description: Those classes are used in the code, but there are no definition for them
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Undefined Classes.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UndefinedClasses.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UndefinedClasses.html","name":"Undefined Classes","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Those classes are used in the code, but there are no definition for them","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Undefined Classes.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Those classes are used in the code, but there are no definition for them.

This may happens under normal conditions, if the application makes use of an unsupported extension, that defines extra classes; 
or if some external libraries, such as PEAR, are not provided during the analysis.



This analysis also checks in attributes.

.. code-block:: php
   
   <?php
   
   // FPDF is a classic PDF class, that is usually omitted by Exakat. 
   $o = new FPDF();
   
   // Exakat reports undefined classes in instanceof
   // PHP ignores them
   if ($o instanceof SomeClass) {
       // doSomething();
   }
   
   // Classes may be used in typehint too
   function foo(TypeHintClass $x) {
       // doSomething();
   }
   
   ?>
Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Fix the typo in the class name
* Add a missing 'use' expression
* Create the missing class
* Added a missing component




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UndefinedClasses                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


