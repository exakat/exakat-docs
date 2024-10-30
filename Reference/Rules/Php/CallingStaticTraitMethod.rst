.. _php-callingstatictraitmethod:

.. _calling-static-trait-method:

Calling Static Trait Method
+++++++++++++++++++++++++++

  Calling directly a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method, defined in a trait is deprecated. It emits a deprecation notice in PHP 8.1.
Calling the same method, from the class point of view is valid.

.. code-block:: php
   
   <?php
   
   trait T {
       public static function t() {
           //
       }
   }
   
   T::t();
   
   ?>

See also `PHP RFC: Deprecations for PHP 8.1 <https://wiki.php.net/rfc/deprecations_php_8_1>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Calling+static+trait+method+Test%3A%3Atest+is+deprecated%2C+it+should+only+be+called+on+a+class+using+the+trait.html>`_



Connex PHP features
-------------------

  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_
  + `static-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/static-method.ini.html>`_


Suggestions
___________

* Call the method from one of the class using the trait
* Move the method to a class




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CallingStaticTraitMethod                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`, :ref:`Deprecated <ruleset-Deprecated>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.5                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and older                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


