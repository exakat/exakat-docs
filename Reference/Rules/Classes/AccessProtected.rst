.. _classes-accessprotected:


.. _access-protected-structures:

Access Protected Structures
+++++++++++++++++++++++++++

.. meta::
	:description:
		Access Protected Structures: It is not allowed to access protected properties, methods or constants from outside the class or its relatives.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Access Protected Structures
	:twitter:description: Access Protected Structures: It is not allowed to access protected properties, methods or constants from outside the class or its relatives
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Access Protected Structures
	:og:type: article
	:og:description: It is not allowed to access protected properties, methods or constants from outside the class or its relatives
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Access Protected Structures.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/AccessProtected.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/AccessProtected.html","name":"Access Protected Structures","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"It is not allowed to access protected properties, methods or constants from outside the class or its relatives","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Access Protected Structures.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

It is not allowed to access protected properties, methods or constants from outside the class or its relatives.

.. code-block:: php
   
   <?php
   
   class foo {
       protected $bar = 1;
   }
   
   $foo = new Foo();
   $foo->bar = 2;
   
   ?>

See also `Visibility <https://www.php.net/manual/en/language.oop5.visibility.php>`_. and `Understanding The Concept Of Visibility In Object Oriented PHP <https://torquemag.io/2016/05/understanding-concept-visibility-object-oriented-php/>`_.

Related PHP errors 
-------------------

  + `Cannot access protected constant %s::%s <https://php-errors.readthedocs.io/en/latest/messages/cannot-access-%25s-constant-%25s%3A%3A%25s.html>`_
  + `Cannot access protected property %s::$%s <https://php-errors.readthedocs.io/en/latest/messages/cannot-access-%25s-property-%25s%3A%3A%24%25s.html>`_
  + `Call to protected method %s::%s from %s%s <https://php-errors.readthedocs.io/en/latest/messages/call-to-%25s-method-%25s%3A%3A%25s%28%29-from-%25s%25s.html>`_



Connex PHP features
-------------------

  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Suggestions
___________

* Change 'protected' to 'public' to relax the constraint
* Add a getter method to reach the target value
* Remove the access to the protected value and find it another way




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/AccessProtected                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


