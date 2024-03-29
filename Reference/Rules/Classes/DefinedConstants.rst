.. _classes-definedconstants:

.. _defined-class-constants:

Defined Class Constants
+++++++++++++++++++++++

  Checks if class constants are defined. This includes class constants, one level of `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ (extended) or interfaces (implemented).

This analysis takes into account native PHP, extension and stubs class definitions.


.. code-block:: php
   
   <?php
   
   class X {
       const Y = 2;
       
       function foo() {
           // This is defined on the line above
           echo self::Y;
   
           // This is not defined in the current code
           echo X::X;
       }
   }
   
   ?>

Specs
_____

+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Classes/DefinedConstants                                                                                                                                                                |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`IsExt <ruleset-IsExt>`, :ref:`IsPHP <ruleset-IsPHP>`, :ref:`IsStub <ruleset-IsStub>`                                            |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                                                                     |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         |                                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      |                                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                               |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features         | class-constant                                                                                                                                                                          |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Configurable by  | php_core, php_extensions, stubs                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


