.. _functions-uselessargument:

.. _useless-argument:

Useless Argument
++++++++++++++++

  The argument is always used with the same value. This value could be hard coded in the method, and save one argument slot.

There is no indication that this argument will be used with other values. It may be a development artifact, that survived without cleaning.
Methods with less than 3 calls are not considered here, to avoid reporting methods used once. Also, arguments with a default value are omitted. 

The chances of useless arguments decrease with the number of usage. The parameter ``maxUsageCount`` prevents highly called methods (more than the parameter value) to be processed.

.. code-block:: php
   
   <?php
   
   // All foo2 arguments are used with different values
   function foo2($a, $b) {}
   foo2(1, 2);
   foo2(2, 2);
   foo2(3, 3);
   
   // The second argument of foo is always used with 2
   function foo($a, $b) {}
   foo(1, 2);
   foo(2, 2);
   foo(3, 2);
   
   ?>

+---------------+---------+---------+---------------------------------------------------------------------------------------+
| Name          | Default | Type    | Description                                                                           |
+---------------+---------+---------+---------------------------------------------------------------------------------------+
| maxUsageCount | 30      | integer | Maximum count of function usage. Use this to limit the amount of processed arguments. |
+---------------+---------+---------+---------------------------------------------------------------------------------------+



See also `class <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.class>`_.


Suggestions
___________

* Remove the argument and hard code its value inside the method
* Add the value as default in the method signature, and drop it from the calls
* Add calls to the method, with more varied arguments




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UselessArgument                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | class                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


