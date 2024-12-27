.. _functions-typehintedreferences:

.. _class-typed-references:

Class-typed References
++++++++++++++++++++++

  Class-typee arguments have no need for references. Since they are representing an object, they are already a reference.

In fact, adding the & on the argument definition may lead to `error <https://www.php.net/error>`_ like ``Only variables should be passed by reference``.

This applies to the ``object`` type hint, but not the the others, such as ``int`` or ``bool``.

.. code-block:: php
   
   <?php
       // a class
       class X {
           public $a = 3;
       }
   
       // typehinted reference
       //function foo(object &$x) works too
       function foo(X &$x) {
           $x->a = 1;
       
           return $x;
       }
   
       // Send an object 
       $y = foo(new X);
   
       // This prints 1;
       print $y->a;
   ?>

See also `Passing by reference <https://www.php.net/manual/en/language.references.pass.php>`_ and `Objects and references <https://www.php.net/manual/en/language.oop5.references.php>`_.

Related PHP errors 
-------------------

  + `Only variables should be passed by reference <https://php-errors.readthedocs.io/en/latest/messages/only-variables-should-be-passed-by-reference.html>`_



Connex PHP features
-------------------

  + `reference <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_


Suggestions
___________

* Remove reference for typehinted arguments, unless the typehint is a scalar typehint.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/TypehintedReferences                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.8                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


