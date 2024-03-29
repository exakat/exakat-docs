.. _structures-couldusematch:

.. _could-use-match:

Could Use Match
+++++++++++++++

  The `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ syntax use may be replaced by a `match() <https://www.php.net/manual/en/control-structures.match.php>`_ call. 

The simplest case for such refactoring is when each of the switch's case (including default), assign one value to the same variable. See this below : 
`Match() <https://www.php.net/manual/en/control-structures.match.php>`_ was introduced in PHP 8. It is not valid with older PHP versions.

.. code-block:: php
   
   <?php
       switch($a) {
           case 1: 
               $b = '1';
               break;
           case 2: 
               $b = '3';
               break;
           default:  
               $b = '0';
               break; 
       }
       
       /*
       $b = match($a) {
           1 => '1',
           2 => '3',
           default => '0'
       };
       */
   ?>

See also `Match() <https://www.php.net/manual/en/control-structures.match.php>`_.


Suggestions
___________

* Replace switch() with match()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldUseMatch                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | match, switch                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


