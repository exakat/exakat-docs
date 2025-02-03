.. _classes-missingabstractmethod:

.. _missing-abstract-method:

Missing Abstract Method
+++++++++++++++++++++++

.. meta::
	:description:
		Missing Abstract Method: Abstract methods must have a non-abstract version for the class to be complete.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Missing Abstract Method
	:twitter:description: Missing Abstract Method: Abstract methods must have a non-abstract version for the class to be complete
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Missing Abstract Method
	:og:type: article
	:og:description: Abstract methods must have a non-abstract version for the class to be complete
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Missing Abstract Method.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MissingAbstractMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MissingAbstractMethod.html","name":"Missing Abstract Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"Abstract methods must have a non-abstract version for the class to be complete","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Missing Abstract Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Abstract methods must have a non-abstract version for the class to be complete. A class that is missing one abstract definition cannot be instantiated.

.. code-block:: php
   
   <?php
   
   // This is a valid definition
   class b extends a {
       function foo() {}
       function bar() {}
   }
   
   // This compiles, but will emit a fatal error if instantiated
   class c extends a {
       function bar() {}
   }
   
   // This illustration lint but doesn't run.
   // moving this class at the beginning of the code will make lint fail
   abstract class a {
       abstract function foo() ;
   }
   
   ?>

See also `Classes Abstraction <https://www.php.net/abstract>`_.

Related PHP errors 
-------------------

  + `Class %s contains %d abstract method and must therefore be declared abstract or implement the remaining methods (%s::%s) <https://php-errors.readthedocs.io/en/latest/messages/class-%25s-contains-%25d-abstract-method%25s-and-must-therefore-be-declared-abstract-or-implement-the-remaining-methods.html>`_



Connex PHP features
-------------------

  + `abstract <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract.ini.html>`_


Suggestions
___________

* Implement the missing methods
* Remove the partially implemented class
* Mark the partially implemented class abstract




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MissingAbstractMethod                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.0                                                                                                                   |
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


