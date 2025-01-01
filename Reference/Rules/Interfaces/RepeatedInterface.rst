.. _interfaces-repeatedinterface:

.. _repeated-interface:

Repeated Interface
++++++++++++++++++

.. meta::
	:description:
		Repeated Interface: A class should implements only once an interface.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Repeated Interface
	:twitter:description: Repeated Interface: A class should implements only once an interface
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Repeated Interface
	:og:type: article
	:og:description: A class should implements only once an interface
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Interfaces/RepeatedInterface.html
	:og:locale: en
A class should implements only once an interface. An interface can only extends once another interface. In both cases, `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ classes or interfaces must be checked.

PHP accepts multiple times the same interface in the ``implements`` clause. In fact, it doesn't do anything beyond the first implement. 
This code may compile, but won't execute.

.. code-block:: php
   
   <?php
   
   use i as j;
   
   interface i {}
   
   // Multiple ways to reference an interface
   class foo implements i, \i, j {}
   
   // This applies to interfaces too
   interface bar extends i, \i, j {}
   
   ?>

See also `Object Interfaces <https://www.php.net/manual/en/language.oop5.interfaces.php>`_ and `The Basics <https://www.php.net/manual/en/language.oop5.basic.php>`_.

Related PHP errors 
-------------------

  + `Class b cannot implement previously implemented interface i <https://php-errors.readthedocs.io/en/latest/messages/class-%25s-cannot-implement-previously-implemented-interface-%25s.html>`_



Connex PHP features
-------------------

  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Suggestions
___________

* Remove the interface usage at the lowest class or interface




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/RepeatedInterface                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.9                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


