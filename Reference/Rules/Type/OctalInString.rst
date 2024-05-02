.. _type-octalinstring:

.. _invalid-octal-in-string:

Invalid Octal In String
+++++++++++++++++++++++

  Any octal sequence inside a string can't be go \377. Those will be a fatal `error <https://www.php.net/error>`_ at parsing time. 

The check is applied to the string, starting with PHP 7.1. In PHP 7.0 and older, those sequences were silently adapted (modulo/% \400).

.. code-block:: php
   
   <?php
   
   // A valid octal in a PHP string
   echo "\100"; // @
   
   // Emit a warning in PHP 7.1
   //Octal escape sequence overflow \500 is greater than \377
   echo "\500"; // @
   
   // Silent conversion
   echo "\478"; // 8
   
   ?>

See also `Integers <https://www.php.net/manual/en/language.types.integer.php>`_.


Suggestions
___________

* Use a double slash to avoid the sequence to be an octal sequence
* Use a function call, such as decoct() to convert larger number to octal notation




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/OctalInString                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>`, :ref:`Inventory <ruleset-Inventory>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.1 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


