.. _namespaces-constantfullyqualified:

.. _fully-qualified-constants:

Fully Qualified Constants
+++++++++++++++++++++++++

  Constants defined with their namespace.

When defining constants with `define() <https://www.php.net/define>`_ function, it is possible to include the actual namespace : 


.. code-block:: php
   
   <?php
   
   define('a\b\c', 1); 
   
   ?>


However, the name should be fully qualified without the initial \. Here, \a\b\c constant will never be accessible as a namespace constant, though it will be accessible via the `constant() <https://www.php.net/constant>`_ function.

Also, the namespace will be absolute, and not a relative namespace of the current one.

Suggestions
___________

* Drop the initial \ when creating constants with define() : for example, use trim($x, '\\'), which removes anti-slashes before and after.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/ConstantFullyQualified                                                                                       |
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
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | namespace                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


