.. _functions-uselesstypecheck:

.. _useless-type-check:

Useless Type Check
++++++++++++++++++

.. meta::
	:description:
		Useless Type Check: With the type system, checking the type of arguments is handled by PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Type Check
	:twitter:description: Useless Type Check: With the type system, checking the type of arguments is handled by PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Type Check
	:og:type: article
	:og:description: With the type system, checking the type of arguments is handled by PHP
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/UselessTypeCheck.html
	:og:locale: en
With the type system, checking the type of arguments is handled by PHP.

In particular, a typed argument can't be null, unless it is explicitly nullable, or has a ``null`` value as default.

.. code-block:: php
   
   <?php
   
   // The test on null is useless, it will never happen
   function foo(A $a) {
       if (is_null($a)) { 
           // do something
       }
   }
   
   // Either nullable ? is too much, either the default null is
   function barbar(?A $a = null) {
   }
   
   // The test on null is useful, the default value null allows it
   function bar(A $a = null) {
       if ($a === null) { 
           // do something
       }
   }
   
   
   ?>

See also `Type Declarations <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_.

Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Suggestions
___________

* Remove the nullable typehint
* Remove the null default value
* Remove tests on null




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UselessTypeCheck                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.9                                                                                                                   |
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


