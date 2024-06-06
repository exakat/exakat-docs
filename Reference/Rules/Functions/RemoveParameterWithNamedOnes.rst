.. _functions-removeparameterwithnamedones:

.. _remove-parameter-with-named-parameters:

Remove Parameter With Named Parameters
++++++++++++++++++++++++++++++++++++++

  It is possible to reduce the size of a method call by using named parameter. This is interesting when some of the positional parameter uses their default value. 

Using named parameters allows the code to drop parameter when it is using the default value. This makes the code less bloated, and the parameter names provide a contextual documentation.

On the other hand, removing an explicit argument makes the code depend on the signature. When that signature changes, so does the code behavior. 


.. code-block:: php
   
   <?php
   
   function foo($a, $b, $c = null);
   
   // This may have one less parameter, with named parameters
   foo(1,2,null);
   
   // using named parameters
   foo(a:1, b:2);
   
   ?>

Specs
_____

+--------------+----------------------------------------+
| Short name   | Functions/RemoveParameterWithNamedOnes |
+--------------+----------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`               |
+--------------+----------------------------------------+
| Exakat since | 2.6.8                                  |
+--------------+----------------------------------------+
| Severity     | Minor                                  |
+--------------+----------------------------------------+
| Time To Fix  | Quick (30 mins)                        |
+--------------+----------------------------------------+
| Precision    | Very high                              |
+--------------+----------------------------------------+
| Available in |                                        |
+--------------+----------------------------------------+


