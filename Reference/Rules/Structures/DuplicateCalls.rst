.. _structures-duplicatecalls:

.. _duplicate-calls:

Duplicate Calls
+++++++++++++++

  Duplicate calls within the same context. They should be called once, and then stashed in a variable for reuse. This saves a lot of time.


.. code-block:: php
   
   <?php
   
   function foo($name) {
       // The name decoration on the string is done twice. Once should be cached in a variable.
       echo "Hello, ".ucfirst(strtolower($name))."<br />";
   
       $query = 'Insert into visitors values ("'.ucfirst(strtolower($name)).'")';
       $res = $db->query($query);
   }
   
   ?>

See also `Userland naming Guide <https://www.php.net/manual/en/userlandnaming.php>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DuplicateCalls                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
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
| Features     | calls                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-duplicated-code <https://github.com/dseguy/clearPHP/tree/master/rules/no-duplicated-code.md>`__                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


