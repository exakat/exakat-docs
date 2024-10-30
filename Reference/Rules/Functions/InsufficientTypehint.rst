.. _functions-insufficienttypehint:

.. _insufficient-typehint:

Insufficient Typehint
+++++++++++++++++++++

  An argument is typehinted, but it actually calls methods, constants or properties that are not listed in the interface.

Classes may be implementing more methods than the one that are listed in the interface they also implements. This means that filtering objects with a typehint, but calling other methods will be solved at execution time : if the method is available, it will be used; if it is not, a fatal `error <https://www.php.net/error>`_ is reported.

Inspired by discussion with `Brandon Savage <https://twitter.com/BrandonSavage>`_.

.. code-block:: php
   
   <?php
   
   class x implements i {
       function methodI() {}
       function notInI() {}
   }
   
   interface i {
       function methodI();
   }
   
   function foo(i $x) {
       $x->methodI(); // this call is valid
       $x->notInI();  // this call is not garanteed
   }
   ?>

See also `Interface segregation principle <https://en.wikipedia.org/wiki/Interface_segregation_principle>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Undefined+constant+y%3A%3AI4.html>`_



Connex PHP features
-------------------

  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_
  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_
  + `abstract-class <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract-class.ini.html>`_


Suggestions
___________

* Extend the interface with the missing called methods
* Change the body of the function to use only the methods that are available in the interface
* Change the used objects so they don't depend on extra methods




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/InsufficientTypehint                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.6                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+


