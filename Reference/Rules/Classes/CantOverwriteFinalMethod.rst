.. _classes-cantoverwritefinalmethod:

.. _can't-overwrite-final-method:

Can't Overwrite Final Method
++++++++++++++++++++++++++++

  A final method is a method that cannot be overwritten in a child class. This means that no class below the current class may define a method with the same name.

.. code-block:: php
   
   <?php
   
   class y extends x { 
       function method() {}
   }
   
   class x { 
       final function method() {}
   }
   
   ?>

Suggestions
___________

* Remove the final keyword in the parent class
* Remove the method in the child class
* Rename the method in the child class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CantOverwriteFinalMethod                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`IsExt <ruleset-IsExt>`, :ref:`IsPHP <ruleset-IsPHP>`, :ref:`IsStub <ruleset-IsStub>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | final, overwrite                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


