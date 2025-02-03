.. _structures-modernempty:


.. _modernize-empty-with-expression:

Modernize Empty With Expression
+++++++++++++++++++++++++++++++


.. meta::

	:description:

		Modernize Empty With Expression: empty() accepts expressions as argument.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Modernize Empty With Expression

	:twitter:description: Modernize Empty With Expression: empty() accepts expressions as argument

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Modernize Empty With Expression

	:og:type: article

	:og:description: empty() accepts expressions as argument

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Modernize Empty With Expression.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ModernEmpty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ModernEmpty.html","name":"Modernize Empty With Expression","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"empty() accepts expressions as argument","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Modernize Empty With Expression.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

empty() accepts expressions as argument. This feature was added in PHP 5.5. 

There is no need to store the expression in a variable before testing, unless it is reused later.

.. code-block:: php
   
   <?php
   
   // PHP 5.5+ empty() usage
   if (empty(foo($b . $c))) {
       doSomethingWithoutA();
   }
   
   // Compatible empty() usage
   $a = foo($b . $c);
   if (empty($a)) {
       doSomethingWithoutA();
   }
   
   // $a2 is reused, storage is legit
   $a2 = strtolower($b . $c);
   if (empty($a2)) {
       doSomething();
   } else {
       echo $a2;
   }
   
   ?>

See also `empty() <https://www.php.net/empty>`_ and `empty() supports arbitrary expressions <https://www.php.net/manual/en/migration55.new-features.php#migration55.new-features.empty>`_.

Connex PHP features
-------------------

  + `empty <https://php-dictionary.readthedocs.io/en/latest/dictionary/empty.ini.html>`_


Suggestions
___________

* Avoid the temporary variable, and use directly empty()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ModernEmpty                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.5 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


