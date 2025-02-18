.. _classes-staticcompatibility:


.. _static-method-compatibility:

Static Method Compatibility
+++++++++++++++++++++++++++

.. meta::
	:description:
		Static Method Compatibility: Once a method has been declared ``static`` or not, it must stay the same in every child class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Static Method Compatibility
	:twitter:description: Static Method Compatibility: Once a method has been declared ``static`` or not, it must stay the same in every child class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Static Method Compatibility
	:og:type: article
	:og:description: Once a method has been declared ``static`` or not, it must stay the same in every child class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Static Method Compatibility.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/StaticCompatibility.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/StaticCompatibility.html","name":"Static Method Compatibility","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 18 Feb 2025 16:28:42 +0000","dateModified":"Tue, 18 Feb 2025 16:28:42 +0000","description":"Once a method has been declared ``static`` or not, it must stay the same in every child class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Static Method Compatibility.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Once a method has been declared ``static`` or not, it must stay the same in every child class. This cannot be changed.

.. code-block:: php
   
   <?php
   
   class X {
       static function foo() {}
              function goo() {}
   }
   
   class Y extends X {
              function foo() {}
       static function goo() {}
   }
   
   ?>
Related PHP errors 
-------------------

  + `Cannot make static method %s::%s() non static in class %s <https://php-errors.readthedocs.io/en/latest/messages/cannot-make-non-static-method-%25s%2F%2F%25s%28%29-static-in-class-%25s.html>`_




Suggestions
___________

* Synchronize the ``static`` keyword on all the eponymous methods.
* Synchronize the absence of the ``static`` keyword on all the eponymous methods.
* Rename methods that needs to change this option.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/StaticCompatibility                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.7.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


