.. _enums-duplicatecasevalue:


.. _duplicate-enum-case-value:

Duplicate Enum Case Value
+++++++++++++++++++++++++

.. meta::
	:description:
		Duplicate Enum Case Value: In a backed enumeration, may it be ``int`` or ``string``, the values of the cases must all be distinct.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Duplicate Enum Case Value
	:twitter:description: Duplicate Enum Case Value: In a backed enumeration, may it be ``int`` or ``string``, the values of the cases must all be distinct
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Duplicate Enum Case Value
	:og:type: article
	:og:description: In a backed enumeration, may it be ``int`` or ``string``, the values of the cases must all be distinct
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Duplicate Enum Case Value.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Enums\/DuplicateCaseValue.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Enums\/DuplicateCaseValue.html","name":"Duplicate Enum Case Value","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"In a backed enumeration, may it be ``int`` or ``string``, the values of the cases must all be distinct","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Duplicate Enum Case Value.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

In a backed enumeration, may it be ``int`` or ``string``, the values of the cases must all be distinct. There can't be two of them of the same value.

.. code-block:: php
   
   <?php
   
   enum e: int {
   	case A = 1 + 1;
   	case B = 2;
   }
   
   enum e2: string {
   	case A = 'A';
   	case B = 'A';
   }
   
   ?>
Related PHP errors 
-------------------

  + `Duplicate value in enum %s for cases %s and %s <https://php-errors.readthedocs.io/en/latest/messages/duplicate-type-%25s-is-redundant.html>`_



Connex PHP features
-------------------

  + `Enumeration (enum) <https://php-dictionary.readthedocs.io/en/latest/dictionary/enum.ini.html>`_
  + `Enumeration Case <https://php-dictionary.readthedocs.io/en/latest/dictionary/enum-case.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Enums/DuplicateCaseValue                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


