.. _exceptions-uselesstry:

.. _useless-try:

Useless Try
+++++++++++

.. meta\:\:
	:description:
		Useless Try: Report try clause that are useless.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Try
	:twitter:description: Useless Try: Report try clause that are useless
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Try
	:og:type: article
	:og:description: Report try clause that are useless
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Exceptions/UselessTry.html
	:og:locale: en
  Report try clause that are useless. A try clause is useless when no `exception <https://www.php.net/exception>`_ is emitted by the code in the block. 



This happens when the underlying layers removed the emission of exceptions.

.. code-block:: php
   
   <?php
   
   try {
   	// Nothing is going to happen here
   	++$a;
   } catch (Exception $e) {
   
   }
   
   ?>

Suggestions
___________

* Remove the Try clause
* Add a throw among the different called methods




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/UselessTry                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
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


