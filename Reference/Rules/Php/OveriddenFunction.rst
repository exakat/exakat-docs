.. _php-overiddenfunction:


.. _php-overridden-function:

PHP Overridden Function
+++++++++++++++++++++++


.. meta::

	:description:

		PHP Overridden Function: It is possible to declare and use a function with the same name as a PHP native, in a namespace.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: PHP Overridden Function

	:twitter:description: PHP Overridden Function: It is possible to declare and use a function with the same name as a PHP native, in a namespace

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: PHP Overridden Function

	:og:type: article

	:og:description: It is possible to declare and use a function with the same name as a PHP native, in a namespace

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP Overridden Function.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/OveriddenFunction.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/OveriddenFunction.html","name":"PHP Overridden Function","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"It is possible to declare and use a function with the same name as a PHP native, in a namespace","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP Overridden Function.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

It is possible to declare and use a function with the same name as a PHP native, in a namespace. 

Within the declaration namespace, it is easy to confuse the local version and the global version, unless the function has been prefixed with ``\``.

When a piece of code use overridden function, any newcomer may be confused by the usage of classic PHP native function in surprising situations. 

It is recommended to avoid redeclare PHP native function in namespaces.

.. code-block:: php
   
   <?php
   
   namespace A {
       use function A\dirname as split;
       
       function dirname($a, $b) { return __FUNCTION__; }
       
       echo dirname('/a/b/c');
       echo split('a', 'b');
       
       echo \dirname('/a/b/c');
   }
   
   ?>
Connex PHP features
-------------------

  + `function <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_


Suggestions
___________

* Change the name of the function, in its declaration and usage.




Specs
_____

+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/OveriddenFunction                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`IsExt <ruleset-IsExt>`, :ref:`IsPHP <ruleset-IsPHP>`, :ref:`IsStub <ruleset-IsStub>`          |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 1.7.6                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                                                                     |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                               |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Configurable by  | php_core, php_extensions, stubs                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


