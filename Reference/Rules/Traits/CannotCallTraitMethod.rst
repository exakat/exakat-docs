.. _traits-cannotcalltraitmethod:

.. _cannot-call-static-trait-method-directly:

Cannot Call Static Trait Method Directly
++++++++++++++++++++++++++++++++++++++++

  From the migration docs : Calling a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method, or accessing a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ property directly on a trait is deprecated. `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods and properties should only be accessed on a class using the trait. 


.. code-block:: php
   
   <?php
    trait t { static public function t() {}}
    a::t();
   // OK
    t::t();
    //Calling static trait method t::t is deprecated, it should only be called on a class using the trait
    
    class a {
       use t;
    }
   
   ?>

See also `Calling a static element on a trait  <https://www.php.net/manual/en/migration81.deprecated.php#migration81.deprecated.core.static-trait>`_.


Suggestions
___________

* Use the trait in a class, and call the method from the class.




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/CannotCallTraitMethod                                                                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.1                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and older                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | trait, static-method                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


