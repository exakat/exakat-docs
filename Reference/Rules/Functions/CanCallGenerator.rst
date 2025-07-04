.. _functions-cancallgenerator:


.. _can't-call-generator:

Can't Call Generator
++++++++++++++++++++

.. meta::
	:description:
		Can't Call Generator: It is not possible to call directly a generator: a generator is a method that uses the ``yield`` or ``yield from`` keyword.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Can't Call Generator
	:twitter:description: Can't Call Generator: It is not possible to call directly a generator: a generator is a method that uses the ``yield`` or ``yield from`` keyword
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Can't Call Generator
	:og:type: article
	:og:description: It is not possible to call directly a generator: a generator is a method that uses the ``yield`` or ``yield from`` keyword
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Can't Call Generator.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/CanCallGenerator.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/CanCallGenerator.html","name":"Can't Call Generator","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"It is not possible to call directly a generator: a generator is a method that uses the ``yield`` or ``yield from`` keyword","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Can't Call Generator.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

It is not possible to call directly a generator: a `generator <https://www.php.net/`generator <https://www.php.net/generator>`_>`_ is a method that uses the ``yield`` or ``yield from`` keyword. 

Such structure shall be used directly in a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ structure, or with the function ``iterator_to_array()``.

.. code-block:: php
   
   <?php
   
   function foo() {
   	echo __FUNCTION__;
   	yield 1;
   }
   
   // Won't display anything, even 'foo'
   foo(); 
   
   // displays both foo and 1
   foreach(foo() as $g) {
   	print $g;
   }
   
   ?>
Connex PHP features
-------------------

  + `Yield <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield.ini.html>`_
  + `yield from Keyword <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield-from.ini.html>`_
  + `Generator <https://php-dictionary.readthedocs.io/en/latest/dictionary/generator.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/CanCallGenerator                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


