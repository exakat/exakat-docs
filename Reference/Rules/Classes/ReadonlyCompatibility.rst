.. _classes-readonlycompatibility:


.. _readonly-property-compatibility:

Readonly Property Compatibility
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		Readonly Property Compatibility: Once a property has been declared ``readonly`` or not, it must stay the same in every child class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Readonly Property Compatibility
	:twitter:description: Readonly Property Compatibility: Once a property has been declared ``readonly`` or not, it must stay the same in every child class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Readonly Property Compatibility
	:og:type: article
	:og:description: Once a property has been declared ``readonly`` or not, it must stay the same in every child class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Readonly Property Compatibility.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ReadonlyCompatibility.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ReadonlyCompatibility.html","name":"Readonly Property Compatibility","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 18 Feb 2025 16:28:42 +0000","dateModified":"Tue, 18 Feb 2025 16:28:42 +0000","description":"Once a property has been declared ``readonly`` or not, it must stay the same in every child class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Readonly Property Compatibility.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Once a property has been declared ``readonly`` or not, it must stay the same in every child class. This cannot be changed.

.. code-block:: php
   
   <?php
   
   class X {
       public readonly int $property;
       public          int $property2;
   }
   
   class Y extends X {
       public          int $property;
       public readonly int $property2;
   }
   
   ?>
Related PHP errors 
-------------------

  + `Cannot redeclare %s property %s::$%s as %s %s::$%s <https://php-errors.readthedocs.io/en/latest/messages/cannot-redeclare-%25s-property-%25s%3A%3A%24%25s-as-%25s-%25s%3A%3A%24%25s.html>`_




Suggestions
___________

* Synchronize the ``readonly`` keyword on all the eponymous properties.
* Synchronize the absence of the ``readonly`` keyword on all the eponymous properties.
* Rename properties that needs to change this option.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ReadonlyCompatibility                                                                                           |
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


