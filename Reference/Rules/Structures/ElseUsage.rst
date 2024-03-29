.. _structures-elseusage:

.. _else-usage:

Else Usage
++++++++++

  Else can be avoided by various means. 

For example, defaulting values before using a condition; returning early in the method, thus skipping long else blocks; using a ternary operator to assign values conditionnaly. 

Else is the equivalent of the default clause in a switch statement. When the if/then structure can be replaced with a switch can (albeit, a 2-case switch seems strange), then else usage is a good solution.

.. code-block:: php
   
   <?php
   
   // $a is always set
   $a = 'default';
   if ($condition) {
       $a = foo($condition);
   }
   
   // Don't use else for default : set default before
   if ($condition) {
       $a = foo($condition);
   } else {
       $a = 'default';
   }
   
   // Use then to exit 
   if ( ! $condition) {
       return;
   }
   $a = foo($condition);
   
   // don't use else to return
   if ($condition) {
       $a = foo($condition);
   } else {
       return;
   }
   
   ?>

See also `Avoid Else, Return Early <http://blog.timoxley.com/post/47041269194/avoid-else-return-early>`_ and `Why does clean code forbid else expression <https://stackoverflow.com/questions/32677046/why-does-clean-code-forbid-else-expression>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ElseUsage                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | class                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


