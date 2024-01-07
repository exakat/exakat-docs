.. _constants-constdefinepreference:

.. _const-or-define-preference:

Const Or Define Preference
++++++++++++++++++++++++++

  ``Const`` and `define() <https://www.php.net/define>`_ have almost the same functional use : they create constants. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make constant definition consistent. 

It is recommended to use ``const`` for global constants, as this keyword is processed at compile time, while `define() <https://www.php.net/define>`_ is executed.

Note that `define() <https://www.php.net/define>`_ used to allow the creation of case-insensitive constants, but this is deprecated since PHP 7.3 and will be removed in PHP 8.0.

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
       
       const B = 3;
       
   ?>

See also `Constant definition <https://www.php.net/const>`_ and `Define <https://www.php.net/define>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/ConstDefinePreference                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | define, const, constant                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


