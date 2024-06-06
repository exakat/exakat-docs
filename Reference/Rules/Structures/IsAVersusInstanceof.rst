.. _structures-isaversusinstanceof:

.. _is\_a()-versus-instanceof:

is_a() Versus instanceof
++++++++++++++++++++++++

  `is_a() <https://www.php.net/is_a>`_ and `instanceof <https://www.php.net/manual/en/language.operators.type.php>`_ have the same functional use: checking if an object is of a specific class. 

The analyzed code has less than 10% of one of them: either `is_a() <https://www.php.net/is_a>`_ or `instanceof <https://www.php.net/manual/en/language.operators.type.php>`_. For consistency reasons, it is recommended to make them all the same. 

It happens that `is_a() <https://www.php.net/is_a>`_ or instance are used depending on coding style and files. One file may be consistently using `is_a() <https://www.php.net/is_a>`_, while the others are all using `instanceof <https://www.php.net/manual/en/language.operators.type.php>`_. 


.. code-block:: php
   
   <?php
   
   if (is_a($object, $class)) { /**/ }
   
   if ($object instanceof $class) { /**/ }
   
   // Note : code is not representative of actual code.
   
   ?>

Suggestions
___________

* Adopt one of the two syntaxes




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IsAVersusInstanceof                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | instanceof                                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


