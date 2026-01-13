.. _variables-strangename:

.. _strange-name-for-variables:

Strange Name For Variables
++++++++++++++++++++++++++

  Variables with strange names. They might be a typo, or bear strange patterns.

Any variable with three identical letter in a row are considered as strange. 2 letters in a row is classic, and while three letters may happen, it is rare enough. 

A list of classic typo is also used to find such variables.

This analysis is case-sensitive.

.. code-block:: php
   
   <?php
   
   class foo {
       function bar() {
           // Strange name $tihs
           return $tihs;
       }
       
       function barbar() {
           // variables with blocks of 3 times the same character are reported
           // Based on Alexandre Joly's tweet
           $aaa = $bab + $www; 
       }
   }
   
   ?>

See also `#QuandLeDevALaFleme <https://twitter.com/bsmt_nevers/status/949238391769653249>`_.

Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_


Suggestions
___________

* Fix the name of the variable
* Rename the variable to something better
* Drop the variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/StrangeName                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.5                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-fuelcms-variables-strangename`, :ref:`case-phpipam-variables-strangename`                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


