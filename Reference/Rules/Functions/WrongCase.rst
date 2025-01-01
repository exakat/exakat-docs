.. _functions-wrongcase:

.. _wrong-function-name-case:

Wrong Function Name Case
++++++++++++++++++++++++

.. meta::
	:description:
		Wrong Function Name Case: The spotted functions are used with a different case than their definition.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong Function Name Case
	:twitter:description: Wrong Function Name Case: The spotted functions are used with a different case than their definition
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong Function Name Case
	:og:type: article
	:og:description: The spotted functions are used with a different case than their definition
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/WrongCase.html
	:og:locale: en
The spotted functions are used with a different case than their definition. While PHP accepts this, it makes the code harder to read. 

It may also be a violation of coding conventions.

.. code-block:: php
   
   <?php
   
   // Definition of the class
   function foo () {}
   
   // Those calls have wrong case
   FOO();
   \Foo();
   
   // This is valid
   foo();
   
   ?>

See also `PHP class name constant case sensitivity and PSR-11 <https://gist.github.com/bcremer/9e8d6903ae38a25784fb1985967c6056>`_.

Connex PHP features
-------------------

  + `case-sensitivity <https://php-dictionary.readthedocs.io/en/latest/dictionary/case-sensitivity.ini.html>`_


Suggestions
___________

* Match the defined functioncall with the called name




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/WrongCase                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


