.. _variables-assignedtwiceormore:

.. _assigned-twice:

Assigned Twice
++++++++++++++

  The same variable is assigned twice in the same function.

While this is possible and quite common, it is also a good practice to avoid changing a value from one literal to another. It is far better to assign the new value to 

Incremental changes to a variables are not reported here.

.. code-block:: php
   
   <?php
   
   function foo() {
       // incremental changes of $a;
       $a = 'a';
       $a++;
       $a = uppercase($a);
       
       $b = 1;
       $c = bar($b);
       // B changed its purpose. Why not call it $d? 
       $b = array(1,2,3);
       
       // This is some forgotten debug
       $e = $config->getSomeList();
       $e = array('OneElement');
   }
   
   ?>

Suggestions
___________

* Remove the first assignation
* Remove the second assignation
* Change the name of the variable in one or both cases




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/AssignedTwiceOrMore                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | variable                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


