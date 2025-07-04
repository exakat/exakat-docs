.. _php-neverkeyword:


.. _never-keyword:

Never Keyword
+++++++++++++

.. meta::
	:description:
		Never Keyword: Never becomes a PHP keyword.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Never Keyword
	:twitter:description: Never Keyword: Never becomes a PHP keyword
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Never Keyword
	:og:type: article
	:og:description: Never becomes a PHP keyword
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Never Keyword.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NeverKeyword.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NeverKeyword.html","name":"Never Keyword","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"Never becomes a PHP keyword","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Never Keyword.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Never becomes a PHP keyword. It is used for typing functions which never returns anything (either dies or throw an `exception) <https://www.php.net/exception>`_.

It should be avoided in namespaces, classes, traits and interfaces. Methods, constants and functions are OK.

.. code-block:: php
   
   <?php
   
   // This is OK
   function never() { } 
   
   // This is no OK
   class never {  } 
   
   ?>

See also `never <https://www.php.net/manual/en/language.types.declarations.php#language.types.declarations.never>`_ and `PHP RFC: noreturn type <https://wiki.php.net/rfc/noreturn_type>`_.

Related PHP errors 
-------------------

  + `Cannot use 'never' as class name as it is reserved <https://php-errors.readthedocs.io/en/latest/messages/cannot-use-%27never%27-as-class-name-as-it-is-reserved.html>`_



Connex PHP features
-------------------

  + `Never Type <https://php-dictionary.readthedocs.io/en/latest/dictionary/never.ini.html>`_


Suggestions
___________

* Rename the classes, traits and interfaces with a different name.




Specs
_____

+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/NeverKeyword                                                                                                                                                                                         |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>` |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.3.0                                                                                                                                                                                                    |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 8.1 and older                                                                                                                                                                                   |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                                                                                    |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                                                                                            |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.1                                                                                                                                                                                                  |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                                |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                  |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


