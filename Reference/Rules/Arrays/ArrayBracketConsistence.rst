.. _arrays-arraybracketconsistence:

.. _array()---[--]-consistence:

Array() / [  ] Consistence
++++++++++++++++++++++++++

  `array() <https://www.php.net/array>`_ or [ ] is the favorite.

`array() <https://www.php.net/array>`_ and [ ] have the same functional use. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same. 

It happens that `array() <https://www.php.net/array>`_ or [] are used depending on coding style and files. One file may be consistently using `array() <https://www.php.net/array>`_, while the others are all using []. 



The only drawback to use [] over `array() <https://www.php.net/array>`_ is backward incompatibility.

.. code-block:: php
   
   <?php
   
   $a = array(1, 2);
   $b = array(array(3, 4), array(5, 6));
   $c = array(array(array(7, 8), array(9, 10)), array(11, 12), array(13, 14)));
   
   // be consistent
   $d = [1, 3];
   ?>

+-------------+---------+---------+-------------------------------------------------------------------------------------------+
| Name        | Default | Type    | Description                                                                               |
+-------------+---------+---------+-------------------------------------------------------------------------------------------+
| array_ratio | 10      | integer | Percentage of arrays in one of the syntaxes, to trigger the other syntax as a violation.  |
+-------------+---------+---------+-------------------------------------------------------------------------------------------+



Suggestions
___________

* Use one syntax consistently.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/ArrayBracketConsistence                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | array                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


