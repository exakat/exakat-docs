.. _constants-isglobalconstant:

.. _is-global-constant:

Is Global Constant
++++++++++++++++++

  Mark a constant that may fallback to a global const definition, even though it is in a namespace. 

This analysis skips PHP and ext's functions, namespaced constants.

.. code-block:: php
   
   <?php
   
   namespace X {
   
       const PHP_VERSION = 1;
       
       // Local constant
       echo PHP_VERSION; 
       
       // This constant fallsback to \E_ALL, unless DNS_NS is defined in this namespace
       echo E_ALL; 
   
       // This constant is always \DNS_NS
       echo \DNS_NS; 
       
       // This is a Notice
       echo UNDEFINED_CONSTANT;
   }
   
   ?>

See also `$GLOBALS <https://www.php.net/manual/en/reserved.variables.globals.php>`_ and `Variable scope <https://www.php.net/manual/en/language.variables.scope.php>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/IsGlobalConstant                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
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
| Features     | constant                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


