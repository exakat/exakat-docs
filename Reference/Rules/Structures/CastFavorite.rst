.. _structures-castfavorite:


.. _favorite-casting-method:

Favorite Casting Method
+++++++++++++++++++++++


.. meta::

	:description:

		Favorite Casting Method: There are two methods for casting : the cast operators, or the conversion functions.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Favorite Casting Method

	:twitter:description: Favorite Casting Method: There are two methods for casting : the cast operators, or the conversion functions

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Favorite Casting Method

	:og:type: article

	:og:description: There are two methods for casting : the cast operators, or the conversion functions

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Favorite Casting Method.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CastFavorite.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CastFavorite.html","name":"Favorite Casting Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"There are two methods for casting : the cast operators, or the conversion functions","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Favorite Casting Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

There are two methods for casting : the cast operators, or the conversion functions. The cast operators are ``int``, ``float`` and ``string``. The conversion functions are ``intval()``, ``floatval()`` and ``strval()``.

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same. 

It happens that casting operators or conversion functions are used depending on coding style and files.

.. code-block:: php
   
   <?php
   
   // be consistent
   $a = (int) $_GET['a'];
   $b = (float) $_GET['b'];
   $c = (int) $_GET['c'];
   $d = (int) $_GET['d'];
   $e = (string) $_GET['e'];
   $f = (int) $_GET['f'];
   $g = (int) $_GET['g'];
   $i = (int) $_GET['i'];
   $j = (int) $_GET['j'];
   $k = (int) $_GET['k'];
   $l = intval($_GET['l']);
   
   ?>
Connex PHP features
-------------------

  + `cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_


Suggestions
___________

* Choose one of the two syntaxes




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CastFavorite                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


