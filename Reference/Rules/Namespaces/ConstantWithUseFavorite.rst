.. _namespaces-constantwithusefavorite:

.. _constant--with-or-without-use:

Constant : With Or Without Use
++++++++++++++++++++++++++++++

  This analysis collects the ways constants are called in the code : with a local import, alias or not, or with their fully qualified name.

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same.

.. code-block:: php
   
   <?php
   
   use const AA as BB;
   
   // This is the fully qualified name. 
   echo \AA;
   
   // If this is used 10 times or more, then it is the standard. 
   echo BB;
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/ConstantWithUseFavorite                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | fully-qualified-name, constant, use                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


