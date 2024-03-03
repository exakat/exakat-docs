.. _attributes-modifyimmutable:

.. _modify-immutable:

Modify Immutable
++++++++++++++++

  A class, marked as immutable, is being modified. 

This `attribute <https://www.php.net/attribute>`_ is supported as a PHPdoc comment, `@immutable, and as a PHP 8.0 `attribute <https://www.php.net/attribute>`_.

.. code-block:: php
   
   <?php
   
   /** @Immutable */
   #[Immutable]
   class x {
       public $x = 1, $y, $z;
   }
   
   $x = new X;
   // $x->x is modified, while it should not
   $x->x = 2 + $x->z;
   
   // $x->z is read only, as expected
   
   ?>

See also `phpstorm-stubs/meta/attributes/Immutable.php <https://github.com/JetBrains/phpstorm-stubs/blob/master/meta/attributes/Immutable.php>`_ and `PhpStorm 2020.3 EAP \#4: Custom PHP 8 Attributes  <https://blog.jetbrains.com/phpstorm/2020/10/phpstorm-2020-3-eap-4/>`_.


Suggestions
___________

* Removed the modification
* Clone the immutable object




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Attributes/ModifyImmutable                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Attributes <ruleset-Attributes>`                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | attribute                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


