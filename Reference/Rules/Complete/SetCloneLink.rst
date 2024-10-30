.. _complete-setclonelink:

.. _set-clone-link:

Set Clone Link
++++++++++++++

  This command creates a link DEFINITION between a clone call, and its equivalent magic method.
This command may not detect all possible link for the clone. It may be missing information about the nature of the clone object.

.. code-block:: php
   
   <?php
   
   class x {
       // Store an object
       private $a;
       
       function foo() {
           // This clone is linked to the magic method below
           return clone $this;
       }
       
       function __clone() {
           $this->a = clone $this->a;
       }
   }
   
   // This is not linked to any __clone method, by lack of information
   clone $x; 
   
   ?>

See also `Object Cloning <https://www.php.net/manual/en/language.oop5.cloning.php>`_.

Connex PHP features
-------------------

  + `clone <https://php-dictionary.readthedocs.io/en/latest/dictionary/clone.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetCloneLink                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


