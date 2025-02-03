.. _php-usetrailingusecomma:


.. _use-closure-trailing-comma:

Use Closure Trailing Comma
++++++++++++++++++++++++++


.. meta::

	:description:

		Use Closure Trailing Comma: Use a trailing comma in the closure's ``use`` list.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Use Closure Trailing Comma

	:twitter:description: Use Closure Trailing Comma: Use a trailing comma in the closure's ``use`` list

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Use Closure Trailing Comma

	:og:type: article

	:og:description: Use a trailing comma in the closure's ``use`` list

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use Closure Trailing Comma.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseTrailingUseComma.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseTrailingUseComma.html","name":"Use Closure Trailing Comma","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Use a trailing comma in the closure's ``use`` list","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use Closure Trailing Comma.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Use a trailing comma in the `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_'s ``use`` list. 

A trailing comma doesn't add any argument, not even a void or null one. It is a convenient for VCS to make diff with the previous code, and have them more readable.

This feature was added in PHP 8.0.

.. code-block:: php
   
   <?php
   
   // PHP 8.0 valid syntax
   $f = function foo() use ($a, ) { };
   
   // always valid syntax for closure
   $f = function foo() use ($a ) { };
   
   ?>

See also `Trailing Comma In Closure Use List <https://wiki.php.net/rfc/trailing_comma_in_closure_use_list>`_.

Connex PHP features
-------------------

  + `trailing-comma <https://php-dictionary.readthedocs.io/en/latest/dictionary/trailing-comma.ini.html>`_


Suggestions
___________

* Add a trailing comma when there are more than one argument in the use expression




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseTrailingUseComma                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.6                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


