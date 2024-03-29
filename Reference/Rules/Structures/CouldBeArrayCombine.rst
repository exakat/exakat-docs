.. _structures-couldbearraycombine:

.. _could-be-array\_combine():

Could Be array_combine()
++++++++++++++++++++++++

  This rule suggests using the native function `array_combine() <https://www.php.net/array_combine>`_ to merge two arrays in a hash. 

.. code-block:: php
   
   <?php
   
   $keys = [1, 2, 3];
   $values = ['a', 'b', 'c'];
   $destination = [];
   foreach($keys as $k => $v) {
   	$destination[$v] = $values[$k];
   }
   
   $destination = [1 => 'a', 2 => 'b', 3 => 'c'];
   
   $destination = array_combine($keys, $values);
   
   ?>

See also `How to use array_merge() and array_combine() in PHP ? <https://www.geeksforgeeks.org/how-to-use-array_merge-and-array_combine-in-php/>`_.


Suggestions
___________

* Use array_combine().




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldBeArrayCombine                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


