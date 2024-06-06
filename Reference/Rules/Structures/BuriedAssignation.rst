.. _structures-buriedassignation:

.. _buried-assignation:

Buried Assignation
++++++++++++++++++

  Those assignations are buried in the code, and placed in unexpected situations. 

They are difficult to spot, and may be confusing. It is advised to place them in a more visible place.

.. code-block:: php
   
   <?php
   
   // $b may be assigned before processing $a
   $a = $c && ($b = 2);
   
   // Display property p immeiately, but also, keeps the object for later
   echo ($o = new x)->p;
   
   // legit syntax, but the double assignation is not obvious.
   for($i = 2, $j = 3; $j < 10; $j++) {
       
   }
   ?>

Suggestions
___________

* Extract the assignation and set it on its own line, prior to the current expression.
* Check if the local variable is necessary




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/BuriedAssignation                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xoops-structures-buriedassignation`, :ref:`case-mautic-structures-buriedassignation`                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


