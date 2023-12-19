.. _structures-sequenceinfor:

.. _sequences-in-for:

Sequences In For
++++++++++++++++

  `For() <https://www.php.net/manual/en/control-structures.for.php>`_ instructions allow several instructions in each of its parameters. Then, the instruction separator is comma ',', not semi-colon, which is used for separating the 3 arguments.


.. code-block:: php
   
   <?php
      for ($a = 0, $b = 0; $a < 10, $b < 20; $a++, $b += 3) {
       // For loop
      }
   ?>


This loop will simultaneously increment `$a` and `$b`. It will stop only when the last of the central sequence reach a value of false : here, when `$b` reach 20 and `$a` will be 6. 

This structure is rarely used, and makes the `for()` instruction quite difficult to read. It is also easy to oversee the multiples instructions, and omit one of them.

It is recommended not to use it.

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SequenceInFor                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Surprising <ruleset-Surprising>`                                                        |
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
| Features     | for                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


