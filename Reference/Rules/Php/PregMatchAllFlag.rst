.. _php-pregmatchallflag:

.. _preg\_match\_all()-flag:

preg_match_all() Flag
+++++++++++++++++++++

  `preg_match_all() <https://www.php.net/preg_match_all>`_ has an option to configure the structure of the results : it is either by capturing parenthesis (by default), or by `result <https://www.php.net/result>`_ sets. 

The second option is the most interesting when the following `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loop has to manipulate several captured strings at the same time. No need to use an index in the first array and use it in the other arrays.


.. code-block:: php
   
   <?php
   $string = 'ababab';
   
   // default behavior
   preg_match_all('/(a)(b)/', $string, $r);
   $found = '';
   foreach($r[1] as $id => $s) {
       $found .= $s.$r[2][$id];
   }
   
   // better behavior
   preg_match_all('/(a)(b)/', $string, $r, PREG_SET_ORDER);
   $found = '';
   foreach($r as $s) {
       $found .= $s[1].$s[2];
   }
   
   ?>


The second syntax is easier to read and may be marginally faster to execute (`preg_match_all() <https://www.php.net/preg_match_all>`_ and `foreach()) <https://www.php.net/manual/en/control-structures.foreach.php>`_.

Suggestions
___________

* Use flags to adapt the results of preg_match_all() to your code, not the contrary.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/PregMatchAllFlag                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-fuelcms-php-pregmatchallflag`                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


