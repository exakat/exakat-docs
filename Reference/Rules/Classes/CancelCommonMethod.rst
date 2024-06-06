.. _classes-cancelcommonmethod:

.. _cancel-common-method:

Cancel Common Method
++++++++++++++++++++

  A `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ method's is too little used in children.

The `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class has a method, which is customised in children classes, though most of the time, those are empty : hence, cancelled. 
A threshold of ``cancelThreshold`` % of the children methods have to be cancelled to report the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class. By default, it is 75 (or 3 out of 4).

.. code-block:: php
   
   <?php
   
   class x {
       abstract function foo();
       abstract function bar();
   }
   
   class y1 extends x {
       function foo() { doSomething(); }
       function bar() { doSomething(); };
   }
   
   class y2 extends x {
       // foo is cancelled : it must be written, but has no use. 
       function foo() {  }
       function bar() { doSomething(); };
   }
   
   ?>

+-----------------+---------+---------+--------------------------------------------------------------------------------+
| Name            | Default | Type    | Description                                                                    |
+-----------------+---------+---------+--------------------------------------------------------------------------------+
| cancelThreshold | 75      | integer | Minimal number of cancelled methods to suggest the cancellation of the parent. |
+-----------------+---------+---------+--------------------------------------------------------------------------------+



Suggestions
___________

* Drop the common method, and the cancelled methods in the children
* Fill the children's methods with actual code




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CancelCommonMethod                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.8                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | class                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+


