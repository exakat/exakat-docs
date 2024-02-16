.. _traits-selfusingtrait:

.. _self-using-trait:

Self Using Trait
++++++++++++++++

  Trait uses itself : this is unnecessary. Traits may use themselves, or be used by other traits, that are using the initial trait itself. 

PHP handles the situation quietly, by ignoring all extra use of the same trait, keeping only one valid version.

.. code-block:: php
   
   <?php
   
   // empty, but valid
   trait a {} 
   
   // obvious self usage
   trait b { use b; }
   
   // less obvious self usage
   trait c { use d, e, f, g, h, c; }
   
   // level 2 self usage
   trait i { use j; }
   trait j { use i; }
   
   ?>

See also `Traits <https://www.php.net/manual/en/language.oop5.traits.php>`_.


Suggestions
___________

* Remove the extra usage of the trait.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/SelfUsingTrait                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Dead code <ruleset-Dead-code>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | trait                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


