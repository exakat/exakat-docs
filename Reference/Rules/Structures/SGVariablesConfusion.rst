.. _structures-sgvariablesconfusion:


.. _static-global-variables-confusion:

Static Global Variables Confusion
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Static Global Variables Confusion: PHP can't have variable that are both static and global variable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Static Global Variables Confusion
	:twitter:description: Static Global Variables Confusion: PHP can't have variable that are both static and global variable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Static Global Variables Confusion
	:og:type: article
	:og:description: PHP can't have variable that are both static and global variable
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Static Global Variables Confusion.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SGVariablesConfusion.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SGVariablesConfusion.html","name":"Static Global Variables Confusion","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP can't have variable that are both static and global variable","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Static Global Variables Confusion.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP can't have variable that are both `static <https://www.php.net/manual/en/language.oop5.static.php>`_ and global variable. While the syntax is legit, the variables will be alternatively global or `static <https://www.php.net/manual/en/language.oop5.static.php>`_.

It is recommended to avoid using the same name for a global variable and a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ variable.

.. code-block:: php
   
   <?php
   
   function foo() {
       $a = 1; // $a is a local variable
       
       global $a; // $a is now a global variable
       
       static $a; // $a is not w static variable 
   }
   
   ?>
Connex PHP features
-------------------

  + `global Scope <https://php-dictionary.readthedocs.io/en/latest/dictionary/global.ini.html>`_
  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Suggestions
___________

* Avoid using static variables
* Avoid using global variables
* Avoid using the same name for static and global variables




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SGVariablesConfusion                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+


