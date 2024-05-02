.. _structures-substrlastarg:

.. _drop-substr-last-arg:

Drop Substr Last Arg
++++++++++++++++++++

  `Substr() <https://www.php.net/substr>`_ works till the end of the string when the last argument is omitted. There is no need to calculate string size to make this work.

.. code-block:: php
   
   <?php
   
   $string = 'abcdef';
   
   // Extract the end of the string
   $cde = substr($string, 2);
   
   // Too much work
   $cde = substr($string, 2, strlen($string));
   
   ?>

Suggestions
___________

* Use negative length
* Omit the last argument to get the string till its end




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SubstrLastArg                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-suitecrm-structures-substrlastarg`, :ref:`case-tine20-structures-substrlastarg`                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


