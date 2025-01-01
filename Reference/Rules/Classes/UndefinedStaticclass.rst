.. _classes-undefinedstaticclass:

.. _undefined-class:

Undefined \:\:class
+++++++++++++++++++

.. meta::
	:description:
		Undefined ::class: ``::class`` doesn't check if a corresponding class exists.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Undefined ::class
	:twitter:description: Undefined ::class: ``::class`` doesn't check if a corresponding class exists
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Undefined ::class
	:og:type: article
	:og:description: ``::class`` doesn't check if a corresponding class exists
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/UndefinedStaticclass.html
	:og:locale: en
``\:\:class`` doesn't check if a corresponding class exists. 

``\:\:class`` must be checked with a call to `class_exists() <https://www.php.net/class_exists>`_. Otherwise, it may lead to a ``Class 'foo' not found`` or even silent dead code : this happens also with Catch and `instanceof <https://www.php.net/manual/en/language.operators.type.php>`_ commands with undefined classes. PHP doesn't raise an `error <https://www.php.net/error>`_ in that case.

.. code-block:: php
   
   <?php
   
   class foo() {}
   
   // prints foo
   echo foo::class; 
   
   // prints bar though bar doesn't exist.
   echo bar::class;
   
   ?>

See also `Class Constants <https://www.php.net/manual/en/language.oop5.constants.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Class+%27x%27+not+found.html>`_



Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Create the missing class
* Fix the name part of the syntax
* Check the name part of syntax with class_exists()




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UndefinedStaticclass                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.5                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


