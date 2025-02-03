.. _structures-indicesareintorstring:


.. _indices-are-int-or-string:

Indices Are Int Or String
+++++++++++++++++++++++++

.. meta::
	:description:
		Indices Are Int Or String: Indices in an array notation such as ``$array['indice']`` may only be integers or string.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Indices Are Int Or String
	:twitter:description: Indices Are Int Or String: Indices in an array notation such as ``$array['indice']`` may only be integers or string
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Indices Are Int Or String
	:og:type: article
	:og:description: Indices in an array notation such as ``$array['indice']`` may only be integers or string
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Indices Are Int Or String.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/IndicesAreIntOrString.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/IndicesAreIntOrString.html","name":"Indices Are Int Or String","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"Indices in an array notation such as ``$array['indice']`` may only be integers or string","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Indices Are Int Or String.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Indices in an array notation such as ``$array['indice']`` may only be integers or string.

Boolean, Null or float are converted to their integer or string equivalent.

Decimal numbers are rounded to the closest integer; ``null`` is transtyped to ``''`` (empty string); true is 1 and false is 0; Integers in strings are transtyped, while partial numbers or decimals are not analyzed in strings. 

As a general rule of thumb, only use integers or strings that don\'t look like integers. 

This analyzer may find constant definitions, when available.

Note also that PHP detects integer inside strings, and silently turn them into integers. Partial and octal numbers are not transformed.

.. code-block:: php
   
   <?php
       $a = [true => 1,
             1.0  => 2,
             1.2  => 3,
             1    => 4,
             '1'  => 5,
             0.8  => 6,
             0x1  => 7,
             01   => 8,
             
             null  => 1,
             ''    => 2,
             
             false => 1,
             0     => 2,
   
             '0.8' => 3,
             '01'  => 4,
             '2a'  => 5
             ];
             
       print_r($a);
   
   /*
   The above displays
   Array
   (
       [1] => 8
       [0] => 2
       [] => 2
       [0.8] => 3
       [01] => 4
       [2a] => 5
   )
   */
   ?>

See also `Arrays syntax <https://www.php.net/manual/en/language.types.array.php>`_.

Related PHP errors 
-------------------

  + `Illegal offset type <https://php-errors.readthedocs.io/en/latest/messages/illegal-offset-type.html>`_



Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Do not use any type but string or integer
* Force typecast the keys when building an array




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IndicesAreIntOrString                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zencart-structures-indicesareintorstring`, :ref:`case-mautic-structures-indicesareintorstring`                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


