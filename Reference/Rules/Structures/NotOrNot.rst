.. _structures-notornot:


.. _not-or-tilde:

Not Or Tilde
++++++++++++

.. meta::
	:description:
		Not Or Tilde: There are two NOT operator in PHP : ``!`` and ``~``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Not Or Tilde
	:twitter:description: Not Or Tilde: There are two NOT operator in PHP : ``!`` and ``~``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Not Or Tilde
	:og:type: article
	:og:description: There are two NOT operator in PHP : ``!`` and ``~``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Not Or Tilde.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NotOrNot.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NotOrNot.html","name":"Not Or Tilde","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"There are two NOT operator in PHP : ``!`` and ``~``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Not Or Tilde.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

There are two NOT operator in PHP : ``!`` and ``~``. The first is a logical operator, and returns a boolean. The second is a bit-wise operator, and flips each bit. 

Although they are distinct operations, there are situations where they provide the same results. In particular, when processing booleans. 

Yet, ``!`` and ``~`` are not the same. ``~`` has a higher priority, and will not yield to ``instanceof``, while ``!`` does.

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same.

.. code-block:: php
   
   <?php
   
   // be consistent
   if (!$condition) {
       doSomething();
   }
   
   if (~$condition) {
       doSomething();
   }
   
   ?>

See also `Bitwise Operators <https://www.php.net/manual/en/language.operators.bitwise.php>`_, `Logical Operators <https://www.php.net/manual/en/language.operators.logical.php>`_ and `Operators Precedences <https://www.php.net/manual/en/language.operators.precedence.php>`_.

Connex PHP features
-------------------

  + `Logical Operators <https://php-dictionary.readthedocs.io/en/latest/dictionary/logical-operator.ini.html>`_
  + `Bitwise Operators <https://php-dictionary.readthedocs.io/en/latest/dictionary/bitwise-operator.ini.html>`_


Suggestions
___________

* Use the ! in logical expressions
* Use the ~ in bitwise expressions, with integers for example




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NotOrNot                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.9                                                                                                                   |
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


