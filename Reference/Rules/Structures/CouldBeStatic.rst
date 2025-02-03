.. _structures-couldbestatic:

.. _could-be-a-static-variable:

Could Be A Static Variable
++++++++++++++++++++++++++

.. meta::
	:description:
		Could Be A Static Variable: This global is only used in one function or method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be A Static Variable
	:twitter:description: Could Be A Static Variable: This global is only used in one function or method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be A Static Variable
	:og:type: article
	:og:description: This global is only used in one function or method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be A Static Variable.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldBeStatic.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldBeStatic.html","name":"Could Be A Static Variable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This global is only used in one function or method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Be A Static Variable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This global is only used in one function or method. It may be transformed into a '`static <https://www.php.net/manual/en/language.oop5.static.php>`_' variable, instead of global. This allows you to keep the value between call to the function, but will not be accessible outside this function.

.. code-block:: php
   
   <?php
   function foo( ) {
       static $variableIsReservedForX; // only accessible within foo( ), even between calls.
       global $variableIsGlobal;       //      accessible everywhere in the application
   }
   ?>
Connex PHP features
-------------------

  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_
  + `static-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/static-variable.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldBeStatic                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolphin-structures-couldbestatic`, :ref:`case-contao-structures-couldbestatic`                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


