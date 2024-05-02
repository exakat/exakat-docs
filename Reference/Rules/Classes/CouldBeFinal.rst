.. _classes-couldbefinal:

.. _class-could-be-final:

Class Could Be Final
++++++++++++++++++++

  Any class that has no extension should be ``final`` by default.

As stated by ``Matthias Noback`` : ``If a class is not marked final, it has at least one subclass``.

Prevent your classes from being subclassed by making them ``final``. Sometimes, classes are not meant or thought to be derivable.

.. code-block:: php
   
   <?php
   
   class x {}            // This class is extended
   class y extends x {}  // This class is extended
   class z extends y {}  // This class is not extended
   
   final class z2 extends y {}  // This class is not extended
   
   ?>

See also `Negative architecture, and assumptions about code <https://matthiasnoback.nl/2018/08/negative-architecture-and-assumptions-about-code/>`_ and `When to declare methods final <https://slamdunk.github.io/blog/when-to-declare-methods-final/>`_.


Suggestions
___________

* Make the class final
* Extends the class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeFinal                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | final                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


