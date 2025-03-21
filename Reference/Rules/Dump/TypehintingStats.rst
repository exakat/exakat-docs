.. _dump-typehintingstats:


.. _typehinting-stats:

Typehinting Stats
+++++++++++++++++

.. meta::
	:description:
		Typehinting Stats: Collects various statistics about typehinting usage.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Typehinting Stats
	:twitter:description: Typehinting Stats: Collects various statistics about typehinting usage
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Typehinting Stats
	:og:type: article
	:og:description: Collects various statistics about typehinting usage
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Typehinting Stats.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/TypehintingStats.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/TypehintingStats.html","name":"Typehinting Stats","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Collects various statistics about typehinting usage","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Typehinting Stats.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Collects various statistics about typehinting usage.

+ totalArguments : Total number of explicit arguments. This count variadics as one, and skip usage of `func_get_args() <https://www.php.net/func_get_args>`_
+ totalFunctions : Total number of functions, closures, arrow-functions and methods
+ withTypehint : Total number of typed arguments
+ withReturnTypehint : Total number of return types
+ scalartype : Total number of scalar type used
+ returnNullable : Total number of `null <https://www.php.net/`null <https://www.php.net/null>`_>`_ types returned
+ argNullable : Total number of `null <https://www.php.net/`null <https://www.php.net/null>`_>`_ types arguments
+ classTypehint : Total number of non-scalar types
+ interfaceTypehint : Total number of interface or abstract class types
+ typedProperties : Total number of typed properties
+ totalProperties : Total number of properties
+ unionTypehints : Total number of union types, including `null <https://www.php.net/`null <https://www.php.net/null>`_>`_ types
+ intersectionTypehints : Total number of intersection types.
Connex PHP features
-------------------

  + `Type System <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/TypehintingStats                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


