.. _enums-undefinedenumcase:

.. _undefined-enumcase:

Undefined Enumcase
++++++++++++++++++

.. meta::
	:description:
		Undefined Enumcase: The enumeration case does not exists.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Undefined Enumcase
	:twitter:description: Undefined Enumcase: The enumeration case does not exists
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Undefined Enumcase
	:og:type: article
	:og:description: The enumeration case does not exists
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Undefined Enumcase.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Enums\/UndefinedEnumcase.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Enums\/UndefinedEnumcase.html","name":"Undefined Enumcase","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"The enumeration case does not exists","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Undefined Enumcase.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The enumeration case does not exists. It may be a class constant, defined in the same enumeration.

.. code-block:: php
   
   <?php
   
   enum theEnum {
       case A; // an enum case
       
       // a constant
       const C = 1;
   }
   
   function foo(theEnum $a) {}
   
   foo(theEnum::A);
   foo(theEnum::C);
   
   ?>
Related PHP errors 
-------------------

  + `Undefined constant <https://php-errors.readthedocs.io/en/latest/messages/undefined-constant-%25s%3A%3A%25s.html>`_



Connex PHP features
-------------------

  + `enum <https://php-dictionary.readthedocs.io/en/latest/dictionary/enum.ini.html>`_
  + `enum-case <https://php-dictionary.readthedocs.io/en/latest/dictionary/enum-case.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Enums/UndefinedEnumcase                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.6                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`unused-enumeration-case`                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


