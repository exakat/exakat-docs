.. _structures-cannotuseappendforreading:

.. _cannot-use-append-for-reading:

Cannot Use Append For Reading
+++++++++++++++++++++++++++++

.. meta::
	:description:
		Cannot Use Append For Reading: The append operator ``[]`` is used to add a value to an array.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Cannot Use Append For Reading
	:twitter:description: Cannot Use Append For Reading: The append operator ``[]`` is used to add a value to an array
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Cannot Use Append For Reading
	:og:type: article
	:og:description: The append operator ``[]`` is used to add a value to an array
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Cannot Use Append For Reading.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CannotUseAppendForReading.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CannotUseAppendForReading.html","name":"Cannot Use Append For Reading","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 16 Jan 2025 17:40:16 +0000","dateModified":"Thu, 16 Jan 2025 17:40:16 +0000","description":"The append operator ``[]`` is used to add a value to an array","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Cannot Use Append For Reading.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The append operator ``[]`` is used to add a value to an array. It doesn't provide an existing value to read. Hence, the short assignement operators, or the increment ones should not be used with the append operator. For example, the coalesce operator yields an `error <https://www.php.net/error>`_ when used with append.

.. code-block:: php
   
   <?php
   
   $x = [];
   $x[] = 1; // normal usage
   $x[] += 2; // adds a 2, but should yield an error
   $x[]++;    // adds a 1, but should yield an error
   // variations with -= *= &= etc.
   
   $x[] ??= 4; // yields a fatal error
   
   ?>
Related PHP errors 
-------------------

  + `Cannot use [] for reading <https://php-errors.readthedocs.io/en/latest/messages/cannot-use-%5B%5D-for-reading.html>`_




Suggestions
___________

* Remove the short assignement and build a real expression on the right hand of the assignement to append




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CannotUseAppendForReading                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.3                                                                                                                   |
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


