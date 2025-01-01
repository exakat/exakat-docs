.. _structures-noneedfortriple:

.. _no-need-for-triple-equal:

No Need For Triple Equal
++++++++++++++++++++++++

.. meta::
	:description:
		No Need For Triple Equal: There is no need for the identity comparison when the methods returns the proper type.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Need For Triple Equal
	:twitter:description: No Need For Triple Equal: There is no need for the identity comparison when the methods returns the proper type
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Need For Triple Equal
	:og:type: article
	:og:description: There is no need for the identity comparison when the methods returns the proper type
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/NoNeedForTriple.html
	:og:locale: en
There is no need for the identity comparison when the methods returns the proper type.

.. code-block:: php
   
   <?php
   
   // foo() returns a string. 
   if ('a' === foo()) {
       // doSomething()
   }
   
   
   function foo() : string { 
       return 'a';
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoNeedForTriple                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.4                                                                                                                   |
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


