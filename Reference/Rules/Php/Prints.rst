.. _php-prints:

.. _displays-text:

Displays Text
+++++++++++++

  Function calls that displays something to the output. Usually, there should not be direct display of data anywhere in the code, but on a specific places, like a template `engine <https://www.php.net/engine>`_, or an output class.

.. code-block:: php
   
   <?php
   
   // Displays de the content of $a
   print $a;
   
   // Displays de the content of $b
   print_r($b);
   
   // Returns de the content of $b, no display.
   $c = var_export($b, true);
   
   ?>
Connex PHP features
-------------------

  + `print <https://php-dictionary.readthedocs.io/en/latest/dictionary/print.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Prints                                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.9                                                                                                                  |
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


