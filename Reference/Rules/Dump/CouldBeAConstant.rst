.. _dump-couldbeaconstant:


.. _could-be-a-constant:

Could Be A Constant
+++++++++++++++++++

.. meta::
	:description:
		Could Be A Constant: This analysis detects literal values that make good candidate for constants.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be A Constant
	:twitter:description: Could Be A Constant: This analysis detects literal values that make good candidate for constants
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be A Constant
	:og:type: article
	:og:description: This analysis detects literal values that make good candidate for constants
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be A Constant.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CouldBeAConstant.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CouldBeAConstant.html","name":"Could Be A Constant","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This analysis detects literal values that make good candidate for constants","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Be A Constant.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This analysis detects literal values that make good candidate for constants. 

Candidates needs two characteristics : 

+ Be assigned as a whole to a container (variable, properties, etc.)
+ Be later (or somewhere else) compared to a container. 

Such literal is used as a token, to handle a state. It is set, then read later. Then, a constant, may it be global or class, is important, so that the relationship between the setting and the reading is maintained throughout the life of the application.

Once the literal is converted into a constant, the value of the literal is not important. It could even be turned into an object. 
Not all literals that are set then read may be turned into a constant : there might be overlap in features by frequently used values (such as `true <https://www.php.net/true>`_, `false <https://www.php.net/false>`_, 0, 1, ) or simple confusion with a local literal. Also, literals that are used for their value (like 1 in a `$a + 1` expression) are not good candidates.

.. code-block:: php
   
   <?php
   
   const SOME_TOKEN = 'abc';
   
   $a = 'some-token';
   $b = SOME_TOKEN; // same as above, as a constant
   
   function foo($arg) {
       if ($arg === 'some-token') {
       
       }
   
       if ($arg === SOME_TOKEN) {
       
       }
   }
   
   ?>

+---------------+---------+---------+---------------------------------------------------------------+
| Name          | Default | Type    | Description                                                   |
+---------------+---------+---------+---------------------------------------------------------------+
| minOccurences | 1       | integer | Minimal number of occurrences of the literal.                 |
+---------------+---------+---------+---------------------------------------------------------------+
| skipString    | ,.php   | array   | List of omitted string values. For example, the empty string. |
+---------------+---------+---------+---------------------------------------------------------------+
| skipInteger   | 1,-0,-1 | array   | List of omitted integer values. By default, 0, 1 and -1.      |
+---------------+---------+---------+---------------------------------------------------------------+


Connex PHP features
-------------------

  + `Constants <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Create the constant and replace all connected literals with it. 




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CouldBeAConstant                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


