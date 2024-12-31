.. _structures-throwsandassign:

.. _throws-an-assignement:

Throws An Assignement
+++++++++++++++++++++

.. meta\:\:
	:description:
		Throws An Assignement: It is possible to throw an exception, and, in the same time, assign this exception to a variable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Throws An Assignement
	:twitter:description: Throws An Assignement: It is possible to throw an exception, and, in the same time, assign this exception to a variable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Throws An Assignement
	:og:type: article
	:og:description: It is possible to throw an exception, and, in the same time, assign this exception to a variable
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/ThrowsAndAssign.html
	:og:locale: en
  It is possible to throw an `exception <https://www.php.net/exception>`_, and, in the same time, assign this `exception <https://www.php.net/exception>`_ to a variable.

However, the variable will never be used, as the `exception <https://www.php.net/exception>`_ is thrown, and any following code is not executed, unless the `exception <https://www.php.net/exception>`_ is caught in the same scope.

.. code-block:: php
   
   <?php
   
       // $e is useful, though not by much
       $e = new() Exception();
       throw $e;
   
       // $e is useless
       throw $e = new Exception();
   
   ?>
Connex PHP features
-------------------

  + `throw <https://php-dictionary.readthedocs.io/en/latest/dictionary/throw.ini.html>`_
  + `assignation <https://php-dictionary.readthedocs.io/en/latest/dictionary/assignation.ini.html>`_


Suggestions
___________

* Drop the assignation




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ThrowsAndAssign                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


