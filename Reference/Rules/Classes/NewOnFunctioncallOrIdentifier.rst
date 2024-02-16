.. _classes-newonfunctioncalloridentifier:

.. _new-on-functioncall-or-identifier:

New On Functioncall Or Identifier
+++++++++++++++++++++++++++++++++

  Object instantiation with new works with or without arguments. Both are valid in PHP. 

The analyzed code has less than 10% of one of the two forms : for consistency reasons, it is recommended to make them all the same.

.. code-block:: php
   
   <?php
   
   $a = new stdClass();
   
   // Parenthesis are used when arguments are compulsory
   $mysql = new MySQLI($host, $user, $pass);
   
   // Parenthesis are omitted when no arguments are available
   // That also makes the instantiation look different
   $b = new stdClass;
   
   ?>

+-----------+---------+---------+---------------------------------------------------------------+
| Name      | Default | Type    | Description                                                   |
+-----------+---------+---------+---------------------------------------------------------------+
| threshold | 10      | integer | Maximal percentage for a syntax to be considered to be fixed. |
+-----------+---------+---------+---------------------------------------------------------------+



Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NewOnFunctioncallOrIdentifier                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | new                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


