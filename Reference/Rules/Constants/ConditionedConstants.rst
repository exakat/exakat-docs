.. _constants-conditionedconstants:

.. _conditioned-constants:

Conditioned Constants
+++++++++++++++++++++

  This rule indicates when a constant is defined if a condition is met. Several definitions of a global constant are possible in the code: using conditions, it is possible to have only one defined during execution.

.. code-block:: php
   
   <?php
   
   if (time() > 1519629617) {
       define('MY_CONST', false);
   } else {
       define('MY_CONST', time() - 1519629617);
   }
   
   ?>
Connex PHP features
-------------------

  + `conditioned <https://php-dictionary.readthedocs.io/en/latest/dictionary/conditioned.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/ConditionedConstants                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
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


