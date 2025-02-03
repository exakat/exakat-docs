.. _structures-notequal:

.. _not-equal-is-not-!==:

Not Equal Is Not !==
++++++++++++++++++++

.. meta::
	:description:
		Not Equal Is Not !==: Not and Equal operators, used separately, don't amount to the different operator ``!==``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Not Equal Is Not !==
	:twitter:description: Not Equal Is Not !==: Not and Equal operators, used separately, don't amount to the different operator ``!==``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Not Equal Is Not !==
	:og:type: article
	:og:description: Not and Equal operators, used separately, don't amount to the different operator ``!==``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Not Equal Is Not !==.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NotEqual.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NotEqual.html","name":"Not Equal Is Not !==","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Not and Equal operators, used separately, don't amount to the different operator ``!==``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Not Equal Is Not !==.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Not and Equal operators, used separately, don't amount to the different operator ``!==``.

``!$a == $b`` first turns ``$a``into the opposite boolean, then compares this boolean value to ``$b``. On the other hand, ``$a !== $b`` compares the two variables for type and value, and returns a boolean. 
Note that the ``instanceof`` operator may be use with this syntax, due to operator precedence.

.. code-block:: php
   
   <?php
   
   if ($string != 'abc') {
       // doSomething()
   }
   
   // Here, string will be an boolean, leading 
   if (!$string == 'abc') {
       // doSomething()
   }
   
   // operator priority may be confusing
   if (!$object instanceof OneClass) {
       // doSomething()
   }
   ?>

See also `Operator Precedence <https://www.php.net/manual/en/language.operators.precedence.php>`_.

Connex PHP features
-------------------

  + `comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/comparison.ini.html>`_


Suggestions
___________

* Use the != or !==
* Use parenthesis




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NotEqual                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.6                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


