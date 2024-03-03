.. _classes-ambiguousvisibilities:

.. _ambiguous-visibilities:

Ambiguous Visibilities
++++++++++++++++++++++

  The properties have the same name, but have different visibilities, across different classes. 

While it is legit to have a property with the same name in different classes, it may easily lead to confusion. As soon as the context is need to understand if the property is accessible or not, the readability suffers.

It is recommended to handle the same properties in the same way across classes, even when the classes are not related.

.. code-block:: php
   
   <?php
   
   class person {
       public $name;
       private $address;
   }
   
   class gangster {
       private $name;
       public $nickname;
       private $address;
   }
   
   $someone = Human::load(123);
   echo 'Hello, '.$someone->name;
   
   ?>

Suggestions
___________

* Sync visibilities for both properties, in the different classes
* Use different names for properties with different usages




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/AmbiguousVisibilities                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Semantics <ruleset-Semantics>`                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | class, visibility                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-typo3-classes-ambiguousvisibilities`                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`missing-visibility`                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


