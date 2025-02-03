.. _classes-couldbeabstractmethod:


.. _could-be-abstract-method:

Could Be Abstract Method
++++++++++++++++++++++++


.. meta::

	:description:

		Could Be Abstract Method: A method can be made abstract, when all the class's children implement it.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Could Be Abstract Method

	:twitter:description: Could Be Abstract Method: A method can be made abstract, when all the class's children implement it

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Could Be Abstract Method

	:og:type: article

	:og:description: A method can be made abstract, when all the class's children implement it

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Abstract Method.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeAbstractMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeAbstractMethod.html","name":"Could Be Abstract Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"A method can be made abstract, when all the class's children implement it","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Be Abstract Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A method can be made abstract, when all the class's children implement it. 

Since the method will also loose its body, it should not be refered in any calls.

.. code-block:: php
   
   <?php
   
   class a {
   	function foo() {}
   
   	function bar() {}
   }
   
   // * for several distinct names 
   class a* extends a {
   	function foo() {}
   }
   
   // a0 only creates foo(), not bar.
   class a0 extends a {
   	function foo() {}
   }
   
   ?>
Connex PHP features
-------------------

  + `abstract <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract.ini.html>`_


Suggestions
___________

* Add the abstract keyword




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeAbstractMethod                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


