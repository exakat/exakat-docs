.. _structures-variablemaybenonglobal:

.. _declare-global-early:

Declare Global Early
++++++++++++++++++++

.. meta::
	:description:
		Declare Global Early: Static and global keywords should be used as early as possible in a method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Declare Global Early
	:twitter:description: Declare Global Early: Static and global keywords should be used as early as possible in a method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Declare Global Early
	:og:type: article
	:og:description: Static and global keywords should be used as early as possible in a method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Declare Global Early.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/VariableMayBeNonGlobal.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/VariableMayBeNonGlobal.html","name":"Declare Global Early","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Static and global keywords should be used as early as possible in a method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Declare Global Early.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`Static <https://www.php.net/manual/en/language.oop5.static.php>`_ and global keywords should be used as early as possible in a method. 

Performance wise, it is better to call ``global`` or ``static`` only before using the variable. 

Human-wise, it is recommended to put ``global`` or ``static`` at the beginning of the method, for better readability.

.. code-block:: php
   
   <?php 
   
   function foo() {
       // $a is not global yet. It is a local variable
       $a = 1;
       // Same for static variables
       $s = 5;
   
       // Now $a is global
       global $a;
       $a = 3;
   
       // Now $s is static
       static $s;
       $s = 55;
   }
   
   ?>

See also `Using static variables <https://www.php.net/manual/en/language.variables.scope.php#language.variables.scope.static>`_ and `The global keyword <https://www.php.net/manual/en/language.variables.scope.php#language.variables.scope.global>`_.

Connex PHP features
-------------------

  + `static-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/static-variable.ini.html>`_
  + `global-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/global-variable.ini.html>`_


Suggestions
___________

* Use static and global at the beginning of the method
* Move static and global to the first usage of the variable
* Remove any access to the variable before static and global




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/VariableMayBeNonGlobal                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


