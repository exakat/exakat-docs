.. _php-alternativesyntax:


.. _php-alternative-syntax:

PHP Alternative Syntax
++++++++++++++++++++++

.. meta::
	:description:
		PHP Alternative Syntax: This rule identifies the usage of alternative syntax in the code, for if then, switch, while, for and foreach.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP Alternative Syntax
	:twitter:description: PHP Alternative Syntax: This rule identifies the usage of alternative syntax in the code, for if then, switch, while, for and foreach
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP Alternative Syntax
	:og:type: article
	:og:description: This rule identifies the usage of alternative syntax in the code, for if then, switch, while, for and foreach
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP Alternative Syntax.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/AlternativeSyntax.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/AlternativeSyntax.html","name":"PHP Alternative Syntax","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This rule identifies the usage of alternative syntax in the code, for if then, switch, while, for and foreach","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP Alternative Syntax.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule identifies the usage of alternative syntax in the code, for if then, switch, while, for and foreach.

Alternative syntax is another way to write the same expression. Alternative syntax is less popular than the normal one, and associated with older coding practices.


.. code-block:: php
   
   <?php
   
   // Normal syntax
   if ($a == 1) { 
       print $a;
   }
   
   // Alternative syntax : identical to the previous one.
   if ($a == 1) : 
       print $a;
   endif;
   
   ?>

See also `Alternative syntax <https://www.php.net/manual/en/control-structures.alternative-syntax.php>`_.

Connex PHP features
-------------------

  + `Alternative Syntax <https://php-dictionary.readthedocs.io/en/latest/dictionary/alternative-syntax.ini.html>`_
  + `Foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_
  + `While <https://php-dictionary.readthedocs.io/en/latest/dictionary/while.ini.html>`_
  + `Do While <https://php-dictionary.readthedocs.io/en/latest/dictionary/do-while.ini.html>`_
  + `For <https://php-dictionary.readthedocs.io/en/latest/dictionary/for.ini.html>`_
  + `Switch <https://php-dictionary.readthedocs.io/en/latest/dictionary/switch.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/AlternativeSyntax                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
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


