.. _php-plusplusonletters:


.. _plus-plus-used-on-strings:

Plus Plus Used On Strings
+++++++++++++++++++++++++

.. meta::
	:description:
		Plus Plus Used On Strings: This rule reports strings that are incremented with the post increment operator ``'s'++``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Plus Plus Used On Strings
	:twitter:description: Plus Plus Used On Strings: This rule reports strings that are incremented with the post increment operator ``'s'++``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Plus Plus Used On Strings
	:og:type: article
	:og:description: This rule reports strings that are incremented with the post increment operator ``'s'++``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Plus Plus Used On Strings.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/PlusPlusOnLetters.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/PlusPlusOnLetters.html","name":"Plus Plus Used On Strings","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"This rule reports strings that are incremented with the post increment operator ``'s'++``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Plus Plus Used On Strings.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports strings that are incremented with the post increment operator ``'s'++``.

This spots issues of the famous feature of PHP : incrementing strings with letters.

This analysis checks for string to be incremented. It doesn't check if the string is a numeric string, but does check the type, implicit or explicit.

.. code-block:: php
   
   <?php
   
   $a = 'a';
   $a++;
   print $a;
   // prints b
   ?>

See also `Incrementing/Decrementing Operators <https://www.php.net/manual/en/language.operators.increment.php>`_ and `Path to Saner Increment/Decrement operators <https://wiki.php.net/rfc/saner-inc-dec-operators>`_.

Connex PHP features
-------------------

  + `String Increment <https://php-dictionary.readthedocs.io/en/latest/dictionary/string-increment.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/PlusPlusOnLetters                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


