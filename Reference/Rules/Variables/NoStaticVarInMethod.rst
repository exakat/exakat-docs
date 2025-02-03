.. _variables-nostaticvarinmethod:


.. _no-static-variable-in-a-method:

No Static Variable In A Method
++++++++++++++++++++++++++++++

.. meta::
	:description:
		No Static Variable In A Method: Refactor static variables into properties.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Static Variable In A Method
	:twitter:description: No Static Variable In A Method: Refactor static variables into properties
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Static Variable In A Method
	:og:type: article
	:og:description: Refactor static variables into properties
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Static Variable In A Method.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/NoStaticVarInMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/NoStaticVarInMethod.html","name":"No Static Variable In A Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Refactor static variables into properties","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Static Variable In A Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Refactor `static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables into properties. 

Inside a class, it is recommended to use the class properties, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or not, to hold values between calls to the method. Inside a function, or a `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, no such container is available, so `static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables may be useful. Although, a refactoring to a class is also recommended here. 

Properties have clear definitions, and are less surprising than `static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables.
The `static <https://www.php.net/manual/en/language.oop5.static.php>`_ variable is easier to refactor as a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ property. It is also possible to refactor it as a property, although it may impact the behavior of the previous code, or require extra work.

.. code-block:: php
   
   <?php
   
   class barbar {
       function foo() {
           static $counter = 0;
           
           // count the number of calls of this method
           return ++$counter;
       }
   }
   
   class bar {
       static $counter = 0;
   
       function foo() {
           // count the number of calls of this method
           return ++self::$counter;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `static-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/static-variable.ini.html>`_


Suggestions
___________

* Refactor the variable into a static property
* Refactor the variable into a property and then use dependency injection




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/NoStaticVarInMethod                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.1                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+


