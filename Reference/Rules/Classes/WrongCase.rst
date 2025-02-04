.. _classes-wrongcase:


.. _wrong-class-name-case:

Wrong Class Name Case
+++++++++++++++++++++

.. meta::
	:description:
		Wrong Class Name Case: The spotted classes are used with a different case than their definition.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong Class Name Case
	:twitter:description: Wrong Class Name Case: The spotted classes are used with a different case than their definition
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong Class Name Case
	:og:type: article
	:og:description: The spotted classes are used with a different case than their definition
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Class Name Case.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/WrongCase.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/WrongCase.html","name":"Wrong Class Name Case","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"The spotted classes are used with a different case than their definition","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Wrong Class Name Case.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The spotted classes are used with a different case than their definition. While PHP accepts this, it makes the code harder to read. 

It may also be a violation of coding conventions.

.. code-block:: php
   
   <?php
   
   // This use statement has wrong case for origin.
   use Foo as X;
   
   // Definition of the class
   class foo {}
   
   // Those instantiations have wrong case
   new FOO();
   new X();
   
   ?>

See also `PHP class name constant case sensitivity and PSR-11 <https://gist.github.com/bcremer/9e8d6903ae38a25784fb1985967c6056>`_.

Connex PHP features
-------------------

  + `Case Sensitivity <https://php-dictionary.readthedocs.io/en/latest/dictionary/case-sensitivity.ini.html>`_
  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Match the defined class name with the called name




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/WrongCase                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Coding conventions <ruleset-Coding-conventions>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-classes-wrongcase`                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


