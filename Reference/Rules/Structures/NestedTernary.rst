.. _structures-nestedternary:

.. _nested-ternary:

Nested Ternary
++++++++++++++

.. meta::
	:description:
		Nested Ternary: Ternary operators should not be nested too deep.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Nested Ternary
	:twitter:description: Nested Ternary: Ternary operators should not be nested too deep
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Nested Ternary
	:og:type: article
	:og:description: Ternary operators should not be nested too deep
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/NestedTernary.html
	:og:locale: en
Ternary operators should not be nested too deep.

They are a convenient instruction to apply some condition, and avoid a if() structure. It works best when it is simple, like in a one liner. 

However, ternary operators tends to make the syntax very difficult to read when they are nested. It is then recommended to use an if() structure, and make the whole code readable.
This is a separate analysis from PHP's preventing nested ternaries without parenthesis.

.. code-block:: php
   
   <?php
   
   // Simple ternary expression
   echo ($a == 1 ? $b : $c) ;
   
   // Nested ternary expressions
   echo ($a === 1 ? $d === 2 ? $b : $d : $d === 3 ? $e : $c) ;
   echo ($a === 1 ? $d === 2 ? $f ===4 ? $g : $h : $d : $d === 3 ? $e : $i === 5 ? $j : $k) ;
   
   //Previous expressions, written as a if / Then expression
   if ($a === 1) {
       if ($d === 2) {
           echo $b;
       } else {
           echo $d;
       }
   } else {
       if ($d === 3) {
           echo $e;
       } else {
           echo $c;
       }
   }
   
   if ($a === 1) {
       if ($d === 2) {
           if ($f === 4) {
               echo $g;
           } else {
               echo $h;
           }
       } else {
           echo $d;
       }
   } else {
       if ($d === 3) {
           echo $e;
       } else {
           if ($i === 5) {
               echo $j;
           } else {
               echo $k;
           }
       }
   }
   
   ?>

+------------------+---------+---------+---------------------------------------------+
| Name             | Default | Type    | Description                                 |
+------------------+---------+---------+---------------------------------------------+
| minNestedTernary | 2       | integer | Minimal number of nested ternary to report. |
+------------------+---------+---------+---------------------------------------------+



See also `Nested Ternaries are Great <https://medium.com/javascript-scene/nested-ternaries-are-great-361bddd0f340>`_ and :ref:`Nested Ternary Without Parenthesis <nested-ternary-without-parenthesis>`.

Connex PHP features
-------------------

  + `ternary <https://php-dictionary.readthedocs.io/en/latest/dictionary/ternary.ini.html>`_


Suggestions
___________

* Replace ternaries by if/then structures.
* Replace ternaries by a functioncall : this provides more readability, offset the actual code, and gives room for making it different.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NestedTernary                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-nested-ternary <https://github.com/dseguy/clearPHP/tree/master/rules/no-nested-ternary.md>`__                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-spip-structures-nestedternary`, :ref:`case-zencart-structures-nestedternary`                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


