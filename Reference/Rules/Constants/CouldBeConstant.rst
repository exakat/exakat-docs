.. _constants-couldbeconstant:


.. _could-be-constant:

Could Be Constant
+++++++++++++++++

.. meta::
	:description:
		Could Be Constant: Literals may be replaced by an existing constant.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Constant
	:twitter:description: Could Be Constant: Literals may be replaced by an existing constant
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Constant
	:og:type: article
	:og:description: Literals may be replaced by an existing constant
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Constant.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/CouldBeConstant.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/CouldBeConstant.html","name":"Could Be Constant","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Literals may be replaced by an existing constant","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Be Constant.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Literals may be replaced by an existing constant. 

Constants makes the code easier to read, as they may bear a meaningful name. They also hide implementation values, with a readable name, such as ``const READABLE= `true <https://www.php.net/true>`_;``. Later, upgrading constant values is easier than scouring the code with a new literal. 

Not all literal can be replaced by a constant values : sometimes, literal may have the same literal value, but different meanings. Check with your application semantics before changing any literal with a constant.

This analysis currently doesn't support arrays. 

This analysis also skips very common values, such as boolean, ``0`` and ``1``. This prevents too many `false <https://www.php.net/false>`_ positives.

.. code-block:: php
   
   <?php
   
       const A = 'abc';
       define('B', 'ab');
       
       class foo {
           const X = 'abcd';
       }
       
       // Could be replaced by B;
       $a = 'ab'; 
       
       // Could be replaced by A;
       $a = 'abc'; 
       
       // Could be replaced by foo::X;
       $a = 'abcd'; 
   
   ?>
Connex PHP features
-------------------

  + `Constants <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Turn the literal into an existing constant




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/CouldBeConstant                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Semantics <ruleset-Semantics>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


