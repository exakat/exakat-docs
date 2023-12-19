.. _constants-defineinsensitivepreference:

.. _constant-case-preference:

Constant Case Preference
++++++++++++++++++++++++

  `Define() <https://www.php.net/define>`_ creates constants which are case sensitive or not. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make constant sensitivity definition consistent. 

Note that `define() <https://www.php.net/define>`_ used to allow the creation of case-sensitive constants, but this is deprecated since PHP 7.3 and will be removed in PHP 8.0.


.. code-block:: php
   
   <?php
   
       define('A1', 1);
       define('A2', 1);
       define('A3', 1);
       define('A4', 1);
       define('A5', 1);
       define('A6', 1);
       define('A7', 1);
       define('A8', 1);
       define('A9', 1);
       define('A10',1);
       
       define('A10',1, true);
       
   ?>

See also `PHP Constants <https://www.php.net/manual/en/language.constants.php>`_ and `Constant definition <https://www.php.net/const>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/DefineInsensitivePreference                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | constant                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


