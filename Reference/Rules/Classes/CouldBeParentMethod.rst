.. _classes-couldbeparentmethod:

.. _could-be-parent-method:

Could Be Parent Method
++++++++++++++++++++++

  A method is defined in several children, but not in a the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class. It may be worth checking if this method doesn't belong the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class, as an abstraction.


.. code-block:: php
   
   <?php
   
   // The parent class
   class x { }
   
   // The children class
   class y1 extends x {
       // foo is common to y1 and y2, so it shall be also a method in x
       function foo() {}
       // fooY1 is specific to y1
       function fooY1() {}
   }
   
   class y2 extends x {
       function foo() {}
       // fooY2 is specific to y1
       function fooY2() {}
   }
   
   ?>


Only the name of the method is used is for gathering purposes. If the code has grown organically, the signature (default values, typehint, argument names) may have followed different path, and will require a refactorisation.

+-------------+---------+---------+-----------------------------------------------+
| Name        | Default | Type    | Description                                   |
+-------------+---------+---------+-----------------------------------------------+
| minChildren | 4       | integer | Minimal number of children using this method. |
+-------------+---------+---------+-----------------------------------------------+



Suggestions
___________

* Create an abstract method in the parent
* Create an concrete method in the parent, and move default behavior there by removing it in children classes




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeParentMethod                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | class, parent                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


