.. _variables-localglobals:


.. _local-globals:

Local Globals
+++++++++++++

.. meta::
	:description:
		Local Globals: A global variable is used locally in a method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Local Globals
	:twitter:description: Local Globals: A global variable is used locally in a method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Local Globals
	:og:type: article
	:og:description: A global variable is used locally in a method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Local Globals.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/LocalGlobals.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/LocalGlobals.html","name":"Local Globals","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A global variable is used locally in a method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Local Globals.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A global variable is used locally in a method. 

Either the global keyword has been forgotten, or the local variable should be renamed in a less ambiguous manner.

Having both a global and a local variable with the same name is legit. PHP keeps the contexts separated, and it processes them independently.

However, in the mind of the coder, it is easy to mistake the local variable $x and the global variable $x. May they be given different meaning, and this is an `error <https://www.php.net/error>`_-prone situation. 

It is recommended to keep the global variables's name distinct from the local variables.

.. code-block:: php
   
   <?php
   
   // This is actualy a global variable
   $variable = 1;
   $globalVariable = 2;
   
   function foo() {
       global $globalVariable2;
       
       $variable = 4;
       $localVariable = 3;
       
       // This always displays 423, instead of 123
       echo $variable .' ' . $globalVariable . ' ' . $localVariable;
   }
   
   ?>
Connex PHP features
-------------------

  + `global Scope <https://php-dictionary.readthedocs.io/en/latest/dictionary/global.ini.html>`_


Suggestions
___________

* Add the global keyword for that variable
* Change the name of the variable for another one, which is not a global variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/LocalGlobals                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


