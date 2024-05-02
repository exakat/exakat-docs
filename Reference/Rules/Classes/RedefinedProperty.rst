.. _classes-redefinedproperty:

.. _redefined-property:

Redefined Property
++++++++++++++++++

  Property redefined in a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class. 

Using heritage, it is possible to define several times the same property, at different levels of the hierarchy.
When this is the case, it is difficult to understand which class will actually handle the property. 

In the case of a private property, the different instances will stay distinct. In the case of protected or public properties, they will all share the same value. 

It is recommended to avoid redefining the same property in a hierarchy.

.. code-block:: php
   
   <?php
   
   class foo {
       protected $aProperty = 1;
   }
   
   class bar extends foo {
       // This property is redefined in the parent class, leading to potential confusion
       protected $aProperty = 1;
   }
   
   ?>

Suggestions
___________

* Remove of the definition




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/RedefinedProperty                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | property                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


