.. _structures-shouldchainexception:

.. _should-chain-exception:

Should Chain Exception
++++++++++++++++++++++

  Chain `exception <https://www.php.net/exception>`_ to provide more context.

When catching an `exception <https://www.php.net/exception>`_ and rethrowing another one, it is recommended to chain the `exception <https://www.php.net/exception>`_ : this means providing the original `exception <https://www.php.net/exception>`_, so that the final recipient has a chance to track the origin of the problem. This doesn't change the thrown message, but provides more information.

Note : Chaining requires PHP > 5.3.0.


.. code-block:: php
   
   <?php
       try {
           throw new Exception('Exception 1', 1);
       } catch (\Exception $e) {
           throw new Exception('Exception 2', 2, $e); 
           // Chaining here. 
   
       }
   ?>

See also `Exception::__construct <https://www.php.net/manual/en/exception.construct.php>`_ and `What are the best practices for catching and re-throwing exceptions? <https://stackoverflow.com/questions/5551668/what-are-the-best-practices-for-catching-and-re-throwing-exceptions/5551828>`_.


Suggestions
___________

* Add the incoming exception to the newly thrown exception




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ShouldChainException                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | exception-chain                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-magento-structures-shouldchainexception`, :ref:`case-tine20-structures-shouldchainexception`                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


