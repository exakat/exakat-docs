.. _functions-noclassastypehint:


.. _no-class-as-type:

No Class As Type
++++++++++++++++

.. meta::
	:description:
		No Class As Type: Avoid using concrete classes as type: always use interfaces or abstract classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Class As Type
	:twitter:description: No Class As Type: Avoid using concrete classes as type: always use interfaces or abstract classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Class As Type
	:og:type: article
	:og:description: Avoid using concrete classes as type: always use interfaces or abstract classes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Class As Type.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NoClassAsTypehint.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NoClassAsTypehint.html","name":"No Class As Type","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Avoid using concrete classes as type: always use interfaces or abstract classes","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Class As Type.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid using concrete classes as type: always use interfaces or abstract classes. This way, different classes, or versions of classes may be passed as argument. The type is not linked to an implementation, but to signatures.

A class is needed when the object is with properties : interfaces do not allow the specifications of properties.

.. code-block:: php
   
   <?php
   
   class X {
       public $p = 1;
   
       function foo() {}
   }
   
   interface i {
       function foo();
   }
   
   // X is a class : any update in the code requires changing / subclassing X or the rest of the code.
   function bar(X $x) {
       $x->foo();
   }
   
   // I is an interface : X may implements this interface without refactoring and pass
   // later, newer versions of X may get another name, but still implement I, and still pass
   function bar2(I $x) {
       $x->foo();
   }
   
   function bar3(I $x) {
       echo $x->p;
   }
   
   ?>

See also `Type hinting for interfaces <http://phpenthusiast.com/object-oriented-php-tutorials/type-hinting-for-interfaces>`_.

Connex PHP features
-------------------

  + `Type System <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_
  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Create an interface with the important methods, and use that interface
* Create an abstract class, when public properties are also needed




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NoClassAsTypehint                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.4                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-vanilla-functions-noclassastypehint`, :ref:`case-phpmyadmin-functions-noclassastypehint`                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


