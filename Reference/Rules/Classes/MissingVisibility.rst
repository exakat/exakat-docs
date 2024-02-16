.. _classes-missingvisibility:

.. _missing-visibility:

Missing Visibility
++++++++++++++++++

  Class constants, properties and methods usage may be controlled by the visibility option. When omitted, it is by default public. 

When omitted, it should be added to make its configuration explicit.

.. code-block:: php
   
   <?php
   
   class x {
       // property is private
       private $property = 1;
   
       // This method is public, and should bear the 'public' option
       function foo() {}
   }
   
   ?>

See also `Visibility <https://www.php.net/manual/en/language.oop5.visibility.php>`_.


Suggestions
___________

* Add the public visibility
* Actually review the code and set a pragmatic visibility
* Set the visibility to private and wait for a request of access




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MissingVisibility                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.5                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Features     | visibility                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`ambiguous-visibilities`                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


