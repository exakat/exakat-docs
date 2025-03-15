.. _classes-newthencall:


.. _new-object-then-immediate-call:

New Object Then Immediate Call
++++++++++++++++++++++++++++++

.. meta::
	:description:
		New Object Then Immediate Call: This rule reports immediate calls on a new object.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: New Object Then Immediate Call
	:twitter:description: New Object Then Immediate Call: This rule reports immediate calls on a new object
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: New Object Then Immediate Call
	:og:type: article
	:og:description: This rule reports immediate calls on a new object
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/New Object Then Immediate Call.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NewThenCall.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NewThenCall.html","name":"New Object Then Immediate Call","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:12:06 +0000","dateModified":"Wed, 05 Mar 2025 15:12:06 +0000","description":"This rule reports immediate calls on a new object","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/New Object Then Immediate Call.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports immediate calls on a new object. This can be simplified with a parenthesis structure. Possibly, inluding an assignation to a local variable, inside the parenthesis.

In PHP 8.4, it is possible to drop the parenthesis altogether.


.. code-block:: php
   
   <?php
   
   // multiline call
   $a = new Foo();
   $a->bar();
   
   // single line call with local variable
   ($a = new Foo())->bar();
   
   // single line call
   (new Foo())->bar();
   
   // PHP 8.4 call 
   new Foo()->bar();
   
   ?>

See also `new MyClass()->method() without parentheses <https://twitter.com/pronskiy/status/1739646806407999653>`_.


Suggestions
___________

* Condense the two expressions into one




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NewThenCall                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                   |
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


