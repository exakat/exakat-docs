.. _classes-cancelcommonmethod:


.. _cancel-common-method:

Cancel Common Method
++++++++++++++++++++

.. meta::
	:description:
		Cancel Common Method: A parent method's is too little used in children.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Cancel Common Method
	:twitter:description: Cancel Common Method: A parent method's is too little used in children
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Cancel Common Method
	:og:type: article
	:og:description: A parent method's is too little used in children
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Cancel Common Method.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CancelCommonMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CancelCommonMethod.html","name":"Cancel Common Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"A parent method's is too little used in children","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Cancel Common Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ method's is too little used in children.

The `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class has a method, which is customised in children classes, though most of the time, those are empty : hence, cancelled. 
A threshold of ``cancelThreshold`` % of the children methods have to be cancelled to report the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class. By default, it is 75 (or 3 out of 4).

.. code-block:: php
   
   <?php
   
   class x {
       abstract function foo();
       abstract function bar();
   }
   
   class y1 extends x {
       function foo() { doSomething(); }
       function bar() { doSomething(); };
   }
   
   class y2 extends x {
       // foo is cancelled : it must be written, but has no use. 
       function foo() {  }
       function bar() { doSomething(); };
   }
   
   ?>

+-----------------+---------+---------+--------------------------------------------------------------------------------+
| Name            | Default | Type    | Description                                                                    |
+-----------------+---------+---------+--------------------------------------------------------------------------------+
| cancelThreshold | 75      | integer | Minimal number of cancelled methods to suggest the cancellation of the parent. |
+-----------------+---------+---------+--------------------------------------------------------------------------------+


Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Drop the common method, and the cancelled methods in the children
* Fill the children's methods with actual code




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CancelCommonMethod                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.8                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+


