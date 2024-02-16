.. _structures-defaultthendiscard:

.. _default-then-discard:

Default Then Discard
++++++++++++++++++++

  Discard the value before assigning it. 

In the code below, the variable is assigned a default value. Then, this value is immediately tested and discarded. 

It is more readable to test the value, and discard it, or assign it later, rather than assign first then discard it later. 


.. code-block:: php
   
   <?php
   
   $a = $a ?? null;
   if ($a === null) {
   	throw new Exception();
   }
   doSomething();
   
   // Alternative code
   
   if (!isset($a) || $a === null) {
   	throw new Exception();
   }
   // $a has a valid value for the purpose
   
   doSomething();
   
   ?>

Suggestions
___________

* Test the value and bail out if it is not valid before assigning it




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DefaultThenDiscard                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | default                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


