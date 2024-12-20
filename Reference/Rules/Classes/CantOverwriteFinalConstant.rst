.. _classes-cantoverwritefinalconstant:

.. _can't-overwrite-final-constant:

Can't Overwrite Final Constant
++++++++++++++++++++++++++++++

  A class constant may be ``final``, and can't be overwritten in a child class. ``final`` is a way to make sure a constant cannot be changed in children classes.

``private`` constants can't be made final, as they are not accessible to any other class. 


.. code-block:: php
   
   <?php
   
   class y extends x { 
       const F = 1;
       const P = 2;
   }
   
   class x { 
       final const F = 3;
       private const PRI = 5; // Private can't be final
       const P = 4;
   }
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/y%3A%3AF+cannot+override+final+constant+x%3A%3AF.html>`_



Connex PHP features
-------------------

  + `final <https://php-dictionary.readthedocs.io/en/latest/dictionary/final.ini.html>`_
  + `overwrite <https://php-dictionary.readthedocs.io/en/latest/dictionary/overwrite.ini.html>`_


Suggestions
___________

* Remove the final keyword in the parent class
* Remove the class constant in the child class
* Rename the class constant in the child class




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CantOverwriteFinalConstant                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.9                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


