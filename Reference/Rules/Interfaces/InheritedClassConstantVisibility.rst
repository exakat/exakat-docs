.. _interfaces-inheritedclassconstantvisibility:

.. _inherited-class-constant-visibility:

Inherited Class Constant Visibility
+++++++++++++++++++++++++++++++++++

  Visibility of class constant must be public, even when overwritten. 

This was not checked until PHP 8.3, where it is now a Fatal `Error <https://www.php.net/error>`_. When the interface and the class are defined in different files, the `error <https://www.php.net/error>`_ appears at execution time.

.. code-block:: php
   
   <?php
   
   interface i {
   	public const I = 1;
   	public const J = 2;
   }
   
   class x implements i {
   	// This should not be possible
   	private const I = 10;
   	public const J = 20;
   }
   
   ?>

Suggestions
___________

* Set the constant visibility in the class to public
* Remove the visibility of the constant in the class




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/InheritedClassConstantVisibility                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>`, :ref:`CompatibilityPHP83 <ruleset-CompatibilityPHP83>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | 8.2                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | visibility, lazy-loading                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+


