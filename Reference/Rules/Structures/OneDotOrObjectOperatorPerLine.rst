.. _structures-onedotorobjectoperatorperline:

.. _one-dot-or-object-operator-per-line:

One Dot Or Object Operator Per Line
+++++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		One Dot Or Object Operator Per Line: Rule #4 of Object Calisthenics : Only one -> or .
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: One Dot Or Object Operator Per Line
	:twitter:description: One Dot Or Object Operator Per Line: Rule #4 of Object Calisthenics : Only one -> or 
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: One Dot Or Object Operator Per Line
	:og:type: article
	:og:description: Rule #4 of Object Calisthenics : Only one -> or 
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/OneDotOrObjectOperatorPerLine.html
	:og:locale: en
  Rule #4 of Object Calisthenics : Only one -> or . per line.
This analysis will also catch the following cases : 
When kept, simple, this rule has some edge cases which are left to the reader.

.. code-block:: php
   
   <?php
   
   // Those should be on different lines for readability
   $a->foo()->bar()->getFinal();
   
   $a->foo()
     ->bar()
     ->getFinal();
   
   // Those should be on different lines for readability
   $concatenation = 'a' . 'b' . $c . 'd';
   
   $concatenation = 'a' . 
                    'b' . 
                    $c .
                    'd';
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OneDotOrObjectOperatorPerLine                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.9                                                                                                                   |
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


