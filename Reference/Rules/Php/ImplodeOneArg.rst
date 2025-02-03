.. _php-implodeonearg:

.. _implode-one-arg:

Implode One Arg
+++++++++++++++

.. meta::
	:description:
		Implode One Arg: implode() may be called with one arg.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Implode One Arg
	:twitter:description: Implode One Arg: implode() may be called with one arg
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Implode One Arg
	:og:type: article
	:og:description: implode() may be called with one arg
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Implode One Arg.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ImplodeOneArg.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ImplodeOneArg.html","name":"Implode One Arg","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"implode() may be called with one arg","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Implode One Arg.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`implode() <https://www.php.net/implode>`_ may be called with one arg. It is recommended to avoid it. 

Using two arguments makes it less surprising to new comers, and consistent with `explode() <https://www.php.net/explode>`_ syntax.

.. code-block:: php
   
   <?php
   
   $array = range('a', 'c');
   
   // empty string is the glue
   print implode('', $array);
   
   // only the array : PHP uses the empty string as glue. 
   // Avoid this
   print implode($array);
   
   ?>

See also `implode <https://www.php.net/implode>`_.


Suggestions
___________

* Add an empty string as first argument




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ImplodeOneArg                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`php-cs-fixable <ruleset-php-cs-fixable>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.7                                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


