.. _structures-ternaryinconcat:

.. _ternary-in-concat:

Ternary In Concat
+++++++++++++++++

.. meta::
	:description:
		Ternary In Concat: Ternary and coalesce operator have higher priority than dot '.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Ternary In Concat
	:twitter:description: Ternary In Concat: Ternary and coalesce operator have higher priority than dot '
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Ternary In Concat
	:og:type: article
	:og:description: Ternary and coalesce operator have higher priority than dot '
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Ternary In Concat.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/TernaryInConcat.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/TernaryInConcat.html","name":"Ternary In Concat","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Ternary and coalesce operator have higher priority than dot '","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Ternary In Concat.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Ternary and coalesce operator have higher priority than dot '.' for concatenation. This means that : 
prints actually ``'E'``, instead of the awaited ``'B0CE'``.

To be safe, always add parenthesis when using ternary operator with concatenation.

.. code-block:: php
   
   <?php
     // print B0CE as expected  
     print 'B'.$b.'C'. ($b > 1 ? 'D') : 'E';
   
     // print E, instead of B0CE
     print 'B'.$b.'C'. $b > 1 ? 'D' : 'E';
   
     print 'B'.$b.'C'. $b > 1 ? 'D' : 'E';
   ?>

See also `Operator Precedence <https://www.php.net/manual/en/language.operators.precedence.php>`_.

Connex PHP features
-------------------

  + `ternary <https://php-dictionary.readthedocs.io/en/latest/dictionary/ternary.ini.html>`_
  + `concatenation <https://php-dictionary.readthedocs.io/en/latest/dictionary/concatenation.ini.html>`_


Suggestions
___________

* Use parenthesis 
* Avoid ternaries and coalesce operators inside a string




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/TernaryInConcat                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-teampass-structures-ternaryinconcat`                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


