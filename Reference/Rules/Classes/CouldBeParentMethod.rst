.. _classes-couldbeparentmethod:


.. _could-be-parent-method:

Could Be Parent Method
++++++++++++++++++++++


.. meta::

	:description:

		Could Be Parent Method: A method is defined in several children, but not in a the parent class.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Could Be Parent Method

	:twitter:description: Could Be Parent Method: A method is defined in several children, but not in a the parent class

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Could Be Parent Method

	:og:type: article

	:og:description: A method is defined in several children, but not in a the parent class

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Parent Method.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeParentMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeParentMethod.html","name":"Could Be Parent Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"A method is defined in several children, but not in a the parent class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Be Parent Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A method is defined in several children, but not in a the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class. It may be worth checking if this method doesn't belong the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class, as an abstraction.
Only the name of the method is used is for gathering purposes. If the code has grown organically, the signature (default values, typehint, argument names) may have followed different path, and will require a refactorisation.

.. code-block:: php
   
   <?php
   
   // The parent class
   class x { }
   
   // The children class
   class y1 extends x {
       // foo is common to y1 and y2, so it shall be also a method in x
       function foo() {}
       // fooY1 is specific to y1
       function fooY1() {}
   }
   
   class y2 extends x {
       function foo() {}
       // fooY2 is specific to y1
       function fooY2() {}
   }
   
   ?>

+-------------+---------+---------+-----------------------------------------------+
| Name        | Default | Type    | Description                                   |
+-------------+---------+---------+-----------------------------------------------+
| minChildren | 4       | integer | Minimal number of children using this method. |
+-------------+---------+---------+-----------------------------------------------+


Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `parent <https://php-dictionary.readthedocs.io/en/latest/dictionary/parent.ini.html>`_


Suggestions
___________

* Create an abstract method in the parent
* Create an concrete method in the parent, and move default behavior there by removing it in children classes




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeParentMethod                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.7                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


