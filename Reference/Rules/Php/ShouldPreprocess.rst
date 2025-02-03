.. _php-shouldpreprocess:


.. _should-preprocess-chr():

Should Preprocess Chr()
+++++++++++++++++++++++

.. meta::
	:description:
		Should Preprocess Chr(): Replace literal chr() calls with their escape sequence.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Preprocess Chr()
	:twitter:description: Should Preprocess Chr(): Replace literal chr() calls with their escape sequence
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Preprocess Chr()
	:og:type: article
	:og:description: Replace literal chr() calls with their escape sequence
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Should Preprocess Chr().html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ShouldPreprocess.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ShouldPreprocess.html","name":"Should Preprocess Chr()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Replace literal chr() calls with their escape sequence","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Should Preprocess Chr().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Replace literal `chr() <https://www.php.net/chr>`_ calls with their escape sequence.

`chr() <https://www.php.net/chr>`_ is a functioncall, that cannot be cached. It is only resolved at execution time. 
On the other hand, literal values are preprocessed by PHP and may be cached.
This is a micro-optimisation.

.. code-block:: php
   
   <?php
   
   // This is easier on PHP
   $a = "\120\110\120\040 is great!";
   
   // This is slow
   $a = chr(80), chr(72), chr(80), chr(32), ' is great!';
   
   // This would be the best with this example, but it is not always possible
   $a = 'PHP is great!';
   
   ?>

See also `Escape sequences <https://www.php.net/manual/en/regexp.reference.escape.php>`_.

Connex PHP features
-------------------

  + `preprocess <https://php-dictionary.readthedocs.io/en/latest/dictionary/preprocess.ini.html>`_


Suggestions
___________

* Use PHP string sequences, and skip chr() at execution time




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ShouldPreprocess                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpadsnew-php-shouldpreprocess`                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


