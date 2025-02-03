.. _php-php80onlytypehints:


.. _php-8.0-only-typehints:

Php 8.0 Only TypeHints
++++++++++++++++++++++


.. meta::

	:description:

		Php 8.0 Only TypeHints: Three scalar typehints are introduced in version 8.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Php 8.0 Only TypeHints

	:twitter:description: Php 8.0 Only TypeHints: Three scalar typehints are introduced in version 8

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Php 8.0 Only TypeHints

	:og:type: article

	:og:description: Three scalar typehints are introduced in version 8

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Php 8.0 Only TypeHints.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php80OnlyTypeHints.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php80OnlyTypeHints.html","name":"Php 8.0 Only TypeHints","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Three scalar typehints are introduced in version 8","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Php 8.0 Only TypeHints.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Three scalar typehints are introduced in version 8.0. They are ``mixed``, ``false`` and ``null``. 

``false`` represents a false boolean, and nothing else. It is more restrictive than a boolean, which accepts true too. 
``null`` is an alternative syntax to ``?`` : it allows the type to be ``null``. 
``mixed`` is an special typehint which explicitly means any type.

An interface ``stringable`` was also introduced to identify objects that may be turned into a string. 

Both the above typehints are to be used in conjunction with other types : they can't be used alone.
In PHP 7.0, both those values could not be used as a class or interface name, to avoid confusion with the actual booleans, nor ``null`` value.

.. code-block:: php
   
   <?php
   
   // function accepts an A object, or null. 
   function foo(A|null $x) {}
   
   // same as above
   function foo2(A|null $x) {}
   
   // returns an object of class B, or false
   function bar($x) : false|B {}
   
   ?>

See also `PHP RFC: Union Types 2.0 <https://wiki.php.net/rfc/union_types_v2>`_.

Connex PHP features
-------------------

  + `mixed <https://php-dictionary.readthedocs.io/en/latest/dictionary/mixed.ini.html>`_
  + `false <https://php-dictionary.readthedocs.io/en/latest/dictionary/false.ini.html>`_
  + `null <https://php-dictionary.readthedocs.io/en/latest/dictionary/null.ini.html>`_


Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php80OnlyTypeHints                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>`, :ref:`CompatibilityPHP73 <ruleset-CompatibilityPHP73>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.9                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


