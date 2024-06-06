.. _classes-isupperfamily:

.. _is-upper-family:

Is Upper Family
+++++++++++++++

  Does the `static <https://www.php.net/manual/en/language.oop5.static.php>`_ call is made within the current hierarchy of class, or, is it made in the class, in the children or outside. 

This applies to `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methodcalls, property accesses and class constants.

.. code-block:: php
   
   <?php
   
   class AAA            { function inAAA() {} }   // upper family : grand-parent
   class AA extends AAA { function inAA()  {} }   // upper family : parent
   class A  extends AA  { function inA()  {} }    // current family
   class B  extends A   { function inB()  {} }    // lower family
   class C              { function inC()  {} }    // outside family
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/IsUpperFamily                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | class                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


