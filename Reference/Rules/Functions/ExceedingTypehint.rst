.. _functions-exceedingtypehint:

.. _exceeding-typehint:

Exceeding Typehint
++++++++++++++++++

  The typehint is not fully used in the method. Some of the defined methods in the typehint are unused. A tighter typehint could be used, to avoid method pollution.
Tight typehint prevents the argument from doing too much. They also require more maintenance : creation of dedicated interfaces, method management to keep all typehint tight.

.. code-block:: php
   
   <?php
   
   interface i {
       function i1();
       function i2();
   }
   
   interface j {
       function j1();
       function j2();
   }
   
   function foo(i $a, j $b) {
       // the i typehint is totally used
       $a->i1();
       $a->i2();
       
       // the i typehint is not totally used : j2() is not used.
       $b->j1();
   }
   
   ?>

See also :ref:`Insufficient Typehint <insufficient-typehint>`.


Suggestions
___________

* Keep the typehint tight, do not inject more than needed.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/ExceedingTypehint                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.3                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Features     | typehint                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


