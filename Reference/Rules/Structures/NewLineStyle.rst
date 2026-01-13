.. _structures-newlinestyle:

.. _new-line-style:

New Line Style
++++++++++++++

  New lines may be written with the sequence \n or with the constant `PHP_EOL <https://www.php.net/PHP_EOL>`_.

When one of those alternatives is used over 90% of the time, it is considered as standard : the remaining are reported.

\n are only located when used alone, in "\n" \(including the double quotes\). When \n is used inside a double-quoted string, its replacement with `PHP_EOL <https://www.php.net/PHP_EOL>`_ would be cumbersome : as such, they are ignored by this analyzer.

.. code-block:: php
   
   <?php
   
   // This may be repeated over 10 times
   $a = "PHP is a great language\n"; 
   $a .= "\n"; 
   
   // This only appears once in the code : this line is reported.
   $b = $a.PHP_EOL.$c; 
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NewLineStyle                                                                                                 |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


