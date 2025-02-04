.. _functions-emptyfunction:


.. _empty-function:

Empty Function
++++++++++++++

.. meta::
	:description:
		Empty Function: Function or method whose body is empty.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Empty Function
	:twitter:description: Empty Function: Function or method whose body is empty
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Empty Function
	:og:type: article
	:og:description: Function or method whose body is empty
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Empty Function.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/EmptyFunction.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/EmptyFunction.html","name":"Empty Function","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"Function or method whose body is empty","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Empty Function.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Function or method whose body is empty. 

Such functions or methods are rarely useful. As a bare minimum, the function should return some useful value, even if constant; it may also throw an `exception <https://www.php.net/exception>`_, trigger an `error <https://www.php.net/error>`_ or simply `die <https://www.php.net/die>`_.

A method is considered empty when it contains nothing and it doesn't overwrite a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_'s method. Constructors with promoted properties are considered non-empty.

Methods which are the concrete version of an abstract method are considered.

.. code-block:: php
   
   <?php
   
   // classic empty function
   function emptyFunction() {}
   
   class bar {
       // classic empty method
       function emptyMethod() {}
   
       // classic empty function
       function emptyMethodWithParent() {}
   }
   
   class barbar extends bar {
       // NOT an empty method : it overwrites the parent method
       function emptyMethodWithParent() {}
   }
   
   ?>
Connex PHP features
-------------------

  + `Functions <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_


Suggestions
___________

* Fill the function with actual code
* Remove any usage of the function, then remove the function




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/EmptyFunction                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-contao-functions-emptyfunction`                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


