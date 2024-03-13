.. _dump-typehintingstats:

.. _typehinting-stats:

Typehinting Stats
+++++++++++++++++

  Collects various statistics about typehinting usage.

+ totalArguments : Total number of explicit arguments. This count variadics as one, and skip usage of `func_get_args() <https://www.php.net/func_get_args>`_
+ totalFunctions : Total number of functions, closures, arrow-functions and methods
+ withTypehint : Total number of typed arguments
+ withReturnTypehint : Total number of return types
+ scalartype : Total number of scalar type used
+ returnNullable : Total number of null types returned
+ argNullable : Total number of null types arguments
+ classTypehint : Total number of non-scalar types
+ interfaceTypehint : Total number of interface or abstract class types
+ typedProperties : Total number of typed properties
+ totalProperties : Total number of properties
+ unionTypehints : Total number of union types, including null types
+ intersectionTypehints : Total number of intersection types

Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/TypehintingStats                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | typehint                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


