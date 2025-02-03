.. _structures-checkalltypes:


.. _check-all-types:

Check All Types
+++++++++++++++

.. meta::
	:description:
		Check All Types: When checking for type, avoid using else.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Check All Types
	:twitter:description: Check All Types: When checking for type, avoid using else
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Check All Types
	:og:type: article
	:og:description: When checking for type, avoid using else
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Check All Types.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CheckAllTypes.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CheckAllTypes.html","name":"Check All Types","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When checking for type, avoid using else","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Check All Types.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When checking for type, avoid using else. Mention explicitly all tested types, and raise an `exception <https://www.php.net/exception>`_ when all available options have been exhausted : after all, this is when the code doesn't know how to handle the datatype.

PHP has a short list of scalar types : null, boolean, integer, real, strings, object, resource and array. When a variable is not holding one the the type, then it may be of any other type. 

Most of the time, when using a simple `is_string() <https://www.php.net/is_string>`_ / else test, this is relying on the conception of the code. By construction, the arguments may be one of two types : array or string. 

What happens often is that in case of failure in the code (database not working, another class not checking its results), a third type is pushed to the structure, and it ends up breaking the execution. 

The safe way is to check the various types all the time, and use the default case (here, the else) to throw `exception() <https://www.php.net/exception>`_ or test an assertion and handle the special case.
Using `is_callable() <https://www.php.net/is_callable>`_, `is_iterable() <https://www.php.net/is_iterable>`_ with this structure is fine : when variable is callable or not, while a variable is an integer or else. 

Using a type test without else is also accepted here. This is a special treatment for this test, and all others are ignored. This aspect may vary depending on situations and projects.

.. code-block:: php
   
   <?php
   
   // hasty version
   if (is_array($argument)) {
       $out = $argument;
   } else {
       // Here, $argument is NOT an array. What if it is an object ? or a NULL ? 
       $out = array($argument);
   }
   
   // Safe type checking : do not assume that 'not an array' means that it is the other expected type.
   if (is_array($argument)) {
       $out = $argument;
   } elseif (is_string($argument)) {
       $out = array($argument);
   } else {
       assert(false, '$argument is not an array nor a string, as expected!');
   }
   
   ?>

Suggestions
___________

* Include a default case to handle all unknown situations
* Include and process explicit types as much as possible




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CheckAllTypes                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.6                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zend-config-structures-checkalltypes`, :ref:`case-vanilla-structures-checkalltypes`                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


