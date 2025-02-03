.. _functions-retypedreference:


.. _retyped-reference:

Retyped Reference
+++++++++++++++++


.. meta::

	:description:

		Retyped Reference: A parameter with a reference may be typed differently, at the end of a method call.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Retyped Reference

	:twitter:description: Retyped Reference: A parameter with a reference may be typed differently, at the end of a method call

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Retyped Reference

	:og:type: article

	:og:description: A parameter with a reference may be typed differently, at the end of a method call

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Retyped Reference.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/RetypedReference.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/RetypedReference.html","name":"Retyped Reference","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A parameter with a reference may be typed differently, at the end of a method call","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Retyped Reference.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A parameter with a reference may be typed differently, at the end of a method call. 

It is possible for a referenced and typed parameter to be retyped during a method call. As such, the type of the used variable might both be checked and changed. 

Using such syntax will lead to confusion in the code.
This works on all types, scalars or objects. 

This rule will detect variables which are defined with a placeholder value, or even undefined, and are filled during the method call.

.. code-block:: php
   
   <?php
   
   $a = [1];
   foo($a);
   echo $a; // Now, $a is a string
   
   function foo(array &$a) {
       $a = "Now, I am a string";
   }
   
   ?>
Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Suggestions
___________

* Do not change a referenced variable's type
* Set the called value to a compatible type.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/RetypedReference                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


