.. _structures-nestedifthen:


.. _nested-ifthen:

Nested Ifthen
+++++++++++++

.. meta::
	:description:
		Nested Ifthen: Nesting ``ifthen`` structures increases the complexity of a method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Nested Ifthen
	:twitter:description: Nested Ifthen: Nesting ``ifthen`` structures increases the complexity of a method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Nested Ifthen
	:og:type: article
	:og:description: Nesting ``ifthen`` structures increases the complexity of a method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Nested Ifthen.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NestedIfthen.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NestedIfthen.html","name":"Nested Ifthen","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"Nesting ``ifthen`` structures increases the complexity of a method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Nested Ifthen.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Nesting ``ifthen`` structures increases the complexity of a method. This rules uses three levels of ifthen to signal a complex structure. When a method has such a command, it should be split into smaller methods.

.. code-block:: php
   
   <?php
   
   function foo($a, $b) {
       if ($a == 1) {
           // Second level, possibly too much already
           if ($b == 2) {
               
           }
       }
   }
   
   function bar($a, $b, $c) {
       if ($a == 1) {
           // Second level. 
           if ($b == 2) {
               // Third level level. 
               if ($c == 3) {
                   // Too much
               }
           }
       }
   }
   
   ?>

+--------------+---------+---------+------------------------------------------------------------+
| Name         | Default | Type    | Description                                                |
+--------------+---------+---------+------------------------------------------------------------+
| nestedIfthen | 3       | integer | Maximal number of acceptable nesting of if-then structures |
+--------------+---------+---------+------------------------------------------------------------+



See also :ref:`No title for Structures/TooManyIf <No anchor for Structures/TooManyIf>`.

Connex PHP features
-------------------

  + `If Then Else <https://php-dictionary.readthedocs.io/en/latest/dictionary/if-then.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NestedIfthen                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-livezilla-structures-nestedifthen`, :ref:`case-mediawiki-structures-nestedifthen`                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


