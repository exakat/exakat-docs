.. _enums-unusedenumcase:


.. _unused-enumeration-case:

Unused Enumeration Case
+++++++++++++++++++++++

.. meta::
	:description:
		Unused Enumeration Case: Those are enumeration cases which are defined, yet not used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Enumeration Case
	:twitter:description: Unused Enumeration Case: Those are enumeration cases which are defined, yet not used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Enumeration Case
	:og:type: article
	:og:description: Those are enumeration cases which are defined, yet not used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unused Enumeration Case.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Enums\/UnusedEnumCase.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Enums\/UnusedEnumCase.html","name":"Unused Enumeration Case","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"Those are enumeration cases which are defined, yet not used","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unused Enumeration Case.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Those are enumeration cases which are defined, yet not used.

The `error <https://www.php.net/error>`_ message when the case is missing mentions a class constant : this is because enumeration cases and class constants use the same configuration. They are only distinguished by their definition, which, here, does not exists.

.. code-block:: php
   
   <?php
   
   enum x {
       case A;
       case C;
       
       const F = 1;
   }
   
   function foo(x $a) {}
   
   foo(x::A);
   
   ?>
Related PHP errors 
-------------------

  + `Undefined constant %s::%s <https://php-errors.readthedocs.io/en/latest/messages/undefined-class-constant-%27%25s%3A%3A%25s%27.html>`_



Connex PHP features
-------------------

  + `Enumeration (enum) <https://php-dictionary.readthedocs.io/en/latest/dictionary/enum.ini.html>`_


Suggestions
___________

* Use the case in the code
* Remove the case in the code
* Fix the name of the case
* Turn the case in a constant




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Enums/UnusedEnumCase                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.0                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`undefined-enumcase`                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


