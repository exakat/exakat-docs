.. _structures-alwaysfalse:

.. _comparison-is-always-the-same:

Comparison Is Always The Same
+++++++++++++++++++++++++++++

.. meta::
	:description:
		Comparison Is Always The Same: Based on the incoming type of arguments, the comparison always yields the same value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Comparison Is Always The Same
	:twitter:description: Comparison Is Always The Same: Based on the incoming type of arguments, the comparison always yields the same value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Comparison Is Always The Same
	:og:type: article
	:og:description: Based on the incoming type of arguments, the comparison always yields the same value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Comparison Is Always The Same.html
	:og:locale: en
Based on the incoming type of arguments, the comparison always yields the same value. The whole condition might be useless.

.. code-block:: php
   
   <?php
   
   function foo(array $a) {
       // This will always fail
       if ($a === 1) {
           
       } elseif (is_int($a)) {
       
       }
   
       // This will always succeed
       if ($a !== null) {
           
       } elseif (is_null($a)) {
           
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/comparison.ini.html>`_


Suggestions
___________

* Remove the constant condition and its corresponding blocks
* Make the constant condition variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/AlwaysFalse                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.4                                                                                                                   |
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


