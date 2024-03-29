.. _classes-redefinedprivateproperty:

.. _redefined-private-property:

Redefined Private Property
++++++++++++++++++++++++++

  Private properties are local to their defined class. PHP doesn't forbid the re-declaration of a private property in a child class.

However, having two or more properties with the same name, in the class hierarchy tends to be `error <https://www.php.net/error>`_ prone. Methods will be accessing properties with the same name, but with different values. 


.. code-block:: php
   
   <?php
   
   class A {
       private $isReady = true;
   }
   
   class B {
       private $isReady = false;
   }
   
   ?>

Suggestions
___________

* Remove the property in the children classes
* Rename the property in the children classes
* Change the visibility in the parent class




Specs
_____

+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name       | Classes/RedefinedPrivateProperty                                                                                        |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`IsExt <ruleset-IsExt>`, :ref:`IsPHP <ruleset-IsPHP>`, :ref:`IsStub <ruleset-IsStub>`    |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 1.2.3                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                     |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                           |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                               |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Features         | private                                                                                                                 |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Configurable by  | php_core, php_extensions, stubs                                                                                         |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples         | :ref:`case-zurmo-classes-redefinedprivateproperty`                                                                      |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-------------------------------------------------------------------------------------------------------------------------+


