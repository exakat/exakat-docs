.. _functions-typehints:

.. _types:

Types
+++++

.. meta::
	:description:
		Types: List of all the types (classes or scalar) used in typing.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Types
	:twitter:description: Types: List of all the types (classes or scalar) used in typing
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Types
	:og:type: article
	:og:description: List of all the types (classes or scalar) used in typing
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Types.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/Typehints.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/Typehints.html","name":"Types","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 24 Jan 2025 10:21:35 +0000","dateModified":"Fri, 24 Jan 2025 10:21:35 +0000","description":"List of all the types (classes or scalar) used in typing","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Types.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>List of all the types (classes or scalar) used in typing.

.. code-block:: php
   
   <?php
   
   // here, array, myObject and string are all typehints.
   function foo(array $array, myObject $x, string $string) { }
   
   ?>

See also `Type declarations <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_.

Connex PHP features
-------------------

  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/Typehints                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


