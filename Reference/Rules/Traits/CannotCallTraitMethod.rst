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

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Calling+static+trait+method+t%3A%3At+is+deprecated%2C+it+should+only+be+called+on+a+class+using+the+trait.html>`_



Connex PHP features
-------------------

  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_
  + `static-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/static-method.ini.html>`_


Suggestions
___________

* Use the trait in a class, and call the method from the class.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/CannotCallTraitMethod                                                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.1                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and older                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


