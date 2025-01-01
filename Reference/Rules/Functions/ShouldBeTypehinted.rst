.. _functions-shouldbetypehinted:

.. _argument-should-be-typehinted:

Argument Should Be Typehinted
+++++++++++++++++++++++++++++

.. meta::
	:description:
		Argument Should Be Typehinted: When a method expects objects as argument, those arguments should be typehinted.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Argument Should Be Typehinted
	:twitter:description: Argument Should Be Typehinted: When a method expects objects as argument, those arguments should be typehinted
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Argument Should Be Typehinted
	:og:type: article
	:og:description: When a method expects objects as argument, those arguments should be typehinted
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/ShouldBeTypehinted.html
	:og:locale: en
When a method expects objects as argument, those arguments should be typehinted. This way, it provides early warning that a wrong object is being sent to the method.

The analyzer will detect situations where a class, or the keywords 'array' or 'callable'. 
`Closure <https://www.php.net/manual/en/class.`closure <https://www.php.net/closure>`_.php>`_ arguments are omitted.

.. code-block:: php
   
   <?php
   
   // What are the possible classes that have a 'foo' method? 
   function foo($bar) {
       return $bar->foo();
   }
   
   ?>

See also `Type declarations <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_.

Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Suggestions
___________

* Add the typehint to the function arguments




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/ShouldBeTypehinted                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `always-typehint <https://github.com/dseguy/clearPHP/tree/master/rules/always-typehint.md>`__                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolphin-functions-shouldbetypehinted`, :ref:`case-mautic-functions-shouldbetypehinted`                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


