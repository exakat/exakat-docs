.. _classes-fossilizedmethod:


.. _fossilized-method:

Fossilized Method
+++++++++++++++++


.. meta::

	:description:

		Fossilized Method: A method is fossilized when it is overwritten so often that changing a default value, a return type or an argument type is getting difficult.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Fossilized Method

	:twitter:description: Fossilized Method: A method is fossilized when it is overwritten so often that changing a default value, a return type or an argument type is getting difficult

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Fossilized Method

	:og:type: article

	:og:description: A method is fossilized when it is overwritten so often that changing a default value, a return type or an argument type is getting difficult

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Fossilized Method.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/FossilizedMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/FossilizedMethod.html","name":"Fossilized Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"A method is fossilized when it is overwritten so often that changing a default value, a return type or an argument type is getting difficult","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Fossilized Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A method is fossilized when it is overwritten so often that changing a default value, a return type or an argument type is getting difficult.

This happens when a class is extended. When a method is overwritten once, it may be easy to update the signature in two places. The more methods are overwriting a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ method, the more difficult it is to update it.

This analysis counts the number of times a method is overwritten, and report any method that is overwritten more than 6 times. This threshold may be configured.

.. code-block:: php
   
   <?php
   
   class x1 {
       // foo1() is never overwritten. It is easy to update.
       function foo1() {}
   
       // foo7() is overwritten seven times. It is hard to update.
       function foo7() {}
   }
   
   // classes x2 to x7, all overwrite foo7();
   // Only x2 is presente here.
   class x2 extends x1 {
       function foo7() {}
   }
   
   ?>

+------------------------+---------+---------+---------------------------------------------------------------------------------+
| Name                   | Default | Type    | Description                                                                     |
+------------------------+---------+---------+---------------------------------------------------------------------------------+
| fossilizationThreshold | 6       | integer | Minimal number of overwriting methods to consider a method difficult to update. |
+------------------------+---------+---------+---------------------------------------------------------------------------------+



See also `Method fossilization <https://www.exakat.io/en/method-fossilisation/>_`.

Connex PHP features
-------------------

  + `fossilized-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/fossilized-method.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/FossilizedMethod                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.6                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


