.. _type-duplicateliteral:


.. _duplicate-literal:

Duplicate Literal
+++++++++++++++++

.. meta::
	:description:
		Duplicate Literal: Report literals that are repeated across the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Duplicate Literal
	:twitter:description: Duplicate Literal: Report literals that are repeated across the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Duplicate Literal
	:og:type: article
	:og:description: Report literals that are repeated across the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Duplicate Literal.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/DuplicateLiteral.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/DuplicateLiteral.html","name":"Duplicate Literal","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Report literals that are repeated across the code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Duplicate Literal.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Report literals that are repeated across the code. The minimum replication is 5, and is configurable with ``maxDuplicate``.

Repeated literals should be considered a prime candidate for constants.

Integer, reals and strings are considered here. Boolean, `Null <https://www.php.net/`null <https://www.php.net/null>`_>`_ and Arrays are omitted. 0, 1, 2, 10 and the empty string are all omitted, as too common. This list of omitted constants may be configured with the ``ignoreList`` parameter : a comma separated list of values.

.. code-block:: php
   
   <?php
       // array index are omitted
       $x[3] = 'b';
   
       // constanst are omitted
       const X = 11;
       define('Y', 'string')
   
       // 0, 1, 2, 10 are omitted
       $x = 0; 
       
   ?>

+--------------+----------+---------+---------------------------------------------------------------+
| Name         | Default  | Type    | Description                                                   |
+--------------+----------+---------+---------------------------------------------------------------+
| minDuplicate | 15       | integer | Minimal number of duplication before the literal is reported. |
+--------------+----------+---------+---------------------------------------------------------------+
| ignoreList   | 0,1,2,10 | array   | Common values that have to be ignored. Comma separated list.  |
+--------------+----------+---------+---------------------------------------------------------------+


Connex PHP features
-------------------

  + `Literal <https://php-dictionary.readthedocs.io/en/latest/dictionary/literal.ini.html>`_


Suggestions
___________

* Create a constant and use it in place of the literal
* Create a class constant and use it in place of the literal




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/DuplicateLiteral                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.6                                                                                                                   |
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


