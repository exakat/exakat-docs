.. _structures-identicalconsecutive:

.. _identical-consecutive-expression:

Identical Consecutive Expression
++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Identical Consecutive Expression: Identical consecutive expressions might be double code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Identical Consecutive Expression
	:twitter:description: Identical Consecutive Expression: Identical consecutive expressions might be double code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Identical Consecutive Expression
	:og:type: article
	:og:description: Identical consecutive expressions might be double code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Identical Consecutive Expression.html
	:og:locale: en
Identical consecutive expressions might be double code. They are worth being checked. 

They may be a copy/paste with unmodified content. When the content has to be duplicated, it is recommended to avoid executing the expression again, and just access the cached `result <https://www.php.net/result>`_.

.. code-block:: php
   
   <?php
   
   $current  = $array[$i];
   $next     = $array[$i + 1];
   $nextnext = $array[$i + 1]; // OOps, nextnext is wrong.
   
   // Initialization
   $previous = foo($array[1]); // previous is initialized with the first value on purpose
   $next     = foo($array[1]); // the second call to foo() with the same arguments should be avoided
   // the above can be rewritten as : 
   $next     = $previous; // save the processing.
   
   for($i = 1; $i < 200; ++$i) {
       $next = doSomething();
   }
   ?>
Connex PHP features
-------------------

  + `expression <https://php-dictionary.readthedocs.io/en/latest/dictionary/expression.ini.html>`_


Suggestions
___________

* Check if the expression needs to be used twice.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IdenticalConsecutive                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


