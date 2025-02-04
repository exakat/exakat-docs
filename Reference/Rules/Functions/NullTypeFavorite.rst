.. _functions-nulltypefavorite:


.. _null-type-favorite:

Null Type Favorite
++++++++++++++++++

.. meta::
	:description:
		Null Type Favorite: Null typed may be written in two ways : with .
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Null Type Favorite
	:twitter:description: Null Type Favorite: Null typed may be written in two ways : with 
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Null Type Favorite
	:og:type: article
	:og:description: Null typed may be written in two ways : with 
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Null Type Favorite.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NullTypeFavorite.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NullTypeFavorite.html","name":"Null Type Favorite","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Null typed may be written in two ways : with ","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Null Type Favorite.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`Null <https://www.php.net/`null <https://www.php.net/null>`_>`_ typed may be written in two ways : with ? or with union type and `null <https://www.php.net/`null <https://www.php.net/null>`_>`_. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same.

.. code-block:: php
   
   <?php
   
   function foo(?A $a) : B|null {
       // some code
   }
   
   ?>
Connex PHP features
-------------------

  + `Null <https://php-dictionary.readthedocs.io/en/latest/dictionary/null.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NullTypeFavorite                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


