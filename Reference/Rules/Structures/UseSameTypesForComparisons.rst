.. _structures-usesametypesforcomparisons:


.. _use-same-types-for-comparisons:

Use Same Types For Comparisons
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Use Same Types For Comparisons: Beware when using inequality operators that the type of the values are the same on both sites of the operators.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Same Types For Comparisons
	:twitter:description: Use Same Types For Comparisons: Beware when using inequality operators that the type of the values are the same on both sites of the operators
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Same Types For Comparisons
	:og:type: article
	:og:description: Beware when using inequality operators that the type of the values are the same on both sites of the operators
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use Same Types For Comparisons.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseSameTypesForComparisons.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseSameTypesForComparisons.html","name":"Use Same Types For Comparisons","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Beware when using inequality operators that the type of the values are the same on both sites of the operators","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use Same Types For Comparisons.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Beware when using inequality operators that the type of the values are the same on both sites of the operators.

Different types may lead to PHP type juggling, where the values are first cast to one of the used types. Other comparisons are always failing, leading to unexpected behavior.

This applies to all inequality operators, as well as the spaceship operator. 



This analysis skips comparisons between integers, floats and strings, as those are usually expected.

Thanks to `Jordi Boggiano <https://twitter.`com <https://www.php.net/com>`_/seldaek>`_ and `Filippo Tessarotto <https://twitter.`com <https://www.php.net/com>`_/slamzoe>`_.

.. code-block:: php
   
   <?php
   
   // Both are wrong, while one should be true (depending on when you read this)
   var_dump('1995-06-08' < new DateTimeImmutable());
   var_dump('1995-06-08' > new DateTimeImmutable());
   
   enum x : int {
       case A = 1;
       case B = 2;
   }
   
   // Both are false as objects are compared, not their integer value
   var_dump(x::A < x::B);
   var_dump(x::A > x::B);
   
   var_dump(x::A->value < x::b->value);
   var_dump(x::A->value > x::b->value);
   
   ?>
Connex PHP features
-------------------

  + `Inequality <https://php-dictionary.readthedocs.io/en/latest/dictionary/inequality.ini.html>`_
  + `Enumeration Case <https://php-dictionary.readthedocs.io/en/latest/dictionary/enum-case.ini.html>`_
  + `Type Juggling <https://php-dictionary.readthedocs.io/en/latest/dictionary/type-juggling.ini.html>`_


Suggestions
___________

* Make sure that the same time




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseSameTypesForComparisons                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                   |
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


