.. _constants-createdoutsideitsnamespace:

.. _constants-created-outside-its-namespace:

Constants Created Outside Its Namespace
+++++++++++++++++++++++++++++++++++++++

  Constants Created Outside Its Namespace.

Using the `define() <https://www.php.net/define>`_ function, it is possible to create constant outside their namespace, but using the fully qualified namespace.


.. code-block:: php
   
   <?php
   
   namespace A\B {
       // define A\B\C as 1
       define('C', 1);
   }
   
   namespace D\E {
       // define A\B\C as 1, while outside the A\B namespace
       define('A\B\C', 1);
   }
   
   ?>


However, this makes the code confusing and difficult to debug. It is recommended to move the constant definition to its namespace.

Suggestions
___________

* Declare the constant in its namespace




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/CreatedOutsideItsNamespace                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | constant                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


