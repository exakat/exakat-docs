.. _classes-clonewithnonobject:

.. _clone-with-non-object:

Clone With Non-Object
+++++++++++++++++++++

  The ``clone`` keyword must be used on variables, properties or results from a function or method call. 

``clone`` cannot be used with constants or literals.


.. code-block:: php
   
   <?php
   
   class x { }
   $x = new x();
   
   // Valid clone
   $y = clone $x;
   
   // Invalid clone
   $y = clone x;
   
   ?>


Cloning a non-object lint but won't execute.

See also `Object cloning <https://www.php.net/manual/en/language.oop5.cloning.php>`_.


Suggestions
___________

* Only clone containers (like variables, properties...)
* Add typehint to injected properties, so they are checked as objects.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CloneWithNonObject                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | clone                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


