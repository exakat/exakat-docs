.. _attributes-usingdeprecated:

.. _using-deprecated-feature:

Using Deprecated Feature
++++++++++++++++++++++++

  Deprecated `attribute <https://www.php.net/attribute>`_ marks a class, interface, trait, enumeration, function, `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, array function, parameter, as a deprecated feature. This rule reports usage of these structure, so they can be removed.

Note that the class ` :ref:`rulesets-deprecated` ` does not need to be defined anywhere.

.. code-block:: php
   
   <?php
   
   #[Deprecated]
   function foo() { }
   
   // This is reported
   foo(); 
   
   ?>

Suggestions
___________

* Remove usage of this deprecated feature, so they can be removed ultimately.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Attributes/UsingDeprecated                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Attributes <ruleset-Attributes>`                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.1                                                                                                                   |
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


