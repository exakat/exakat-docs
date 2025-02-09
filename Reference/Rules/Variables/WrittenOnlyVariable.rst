.. _variables-writtenonlyvariable:


.. _written-only-variables:

Written Only Variables
++++++++++++++++++++++

.. meta::
	:description:
		Written Only Variables: Those variables are being written, but never read.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Written Only Variables
	:twitter:description: Written Only Variables: Those variables are being written, but never read
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Written Only Variables
	:og:type: article
	:og:description: Those variables are being written, but never read
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Written Only Variables.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/WrittenOnlyVariable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/WrittenOnlyVariable.html","name":"Written Only Variables","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Those variables are being written, but never read","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Written Only Variables.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Those variables are being written, but never read. In this way, they are useless and should be removed, or be read at some point in the code.

When the variables are only written, it takes time to process them, while discarding their `result <https://www.php.net/result>`_ without usage. Also, when those variables are built with a complex process, it makes it difficult to understand their point, and still create maintenance work.

.. code-block:: php
   
   <?php
   
   // $a is used multiple times, but never read
   $a = 'a';
   $a .= 'b';
   
   $b = 3; 
   //$b is actually read once
   $a .= $b + 3; 
   
   ?>
Connex PHP features
-------------------

  + `Variables <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_


Suggestions
___________

* Check that variables are written AND read in each context
* Remove variables that are only read
* Use the variable that are only read




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/WrittenOnlyVariable                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-unused-variable <https://github.com/dseguy/clearPHP/tree/master/rules/no-unused-variable.md>`__                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolibarr-variables-writtenonlyvariable`, :ref:`case-suitecrm-variables-writtenonlyvariable`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


