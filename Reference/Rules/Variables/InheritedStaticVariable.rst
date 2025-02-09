.. _variables-inheritedstaticvariable:


.. _inherited-static-variable:

Inherited Static Variable
+++++++++++++++++++++++++

.. meta::
	:description:
		Inherited Static Variable: Static variables are distinct when used in an inherited static method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Inherited Static Variable
	:twitter:description: Inherited Static Variable: Static variables are distinct when used in an inherited static method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Inherited Static Variable
	:og:type: article
	:og:description: Static variables are distinct when used in an inherited static method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Inherited Static Variable.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/InheritedStaticVariable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/InheritedStaticVariable.html","name":"Inherited Static Variable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Static variables are distinct when used in an inherited static method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Inherited Static Variable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`Static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables are distinct when used in an inherited `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method. In PHP 8.1, the `static <https://www.php.net/manual/en/language.oop5.static.php>`_ variable will also be inherited, and shared between the two methods, like a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ property.

.. code-block:: php
   
   <?php
   
   // Code extracted from the RFC
   class A {
       public static function counter() {
           static $i = 0;
           return ++$i;
       }
   }
   class B extends A {}
    
   var_dump(A::counter()); // int(1)
   var_dump(A::counter()); // int(2)
   var_dump(B::counter()); // int(1)
   var_dump(B::counter()); // int(2)
   
   ?>

See also `PHP RFC: Static variables in inherited methods <https://wiki.php.net/rfc/static_variable_inheritance>`_.

Connex PHP features
-------------------

  + `Static Variables <https://php-dictionary.readthedocs.io/en/latest/dictionary/static-variable.ini.html>`_
  + `Inheritance <https://php-dictionary.readthedocs.io/en/latest/dictionary/inheritance.ini.html>`_


Suggestions
___________

* Define the method in the child class to enforce the distinct behavior
* Replace the static variable by a static property to make this PHP 8.1 ready




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Variables/InheritedStaticVariable                                                                                                    |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.2.2                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 8.0 and older                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.1                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Medium                                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


