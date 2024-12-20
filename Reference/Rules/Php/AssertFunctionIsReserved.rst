.. _php-assertfunctionisreserved:

.. _assert-function-is-reserved:

Assert Function Is Reserved
+++++++++++++++++++++++++++

  Avoid defining an ``assert`` function in namespaces. 

While they work fine when the assertions are active (``zend.assertions=1``), calls to unqualified ``assert`` are optimized away when assertions are not active. 

Since PHP 7.3, a fatal `error <https://www.php.net/error>`_ is emitted : ``Defining a custom `assert() <https://www.php.net/assert>`_ function is deprecated, as the function has special semantics``.

.. code-block:: php
   
   <?php
   //      Run this with zend.assertions=1 and 
   // Then run this with zend.assertions=0
   
   namespace Test {
       function assert() {
           global $foo;
   
           $foo = true;
       }
   }
   
   namespace Test {
       assert();
   
       var_dump(isset($foo));
   }
   
   ?>

See also `assert <https://www.php.net/assert>`_ and `User-defined assert function is optimized away with zend.assertions=-1 <https://bugs.php.net/bug.php?id=75445>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Defining+a+custom+assert%28%29+function+is+deprecated%2C+as+the+function+has+special+semantics.html>`_



Connex PHP features
-------------------

  + `assertion <https://php-dictionary.readthedocs.io/en/latest/dictionary/assertion.ini.html>`_


Suggestions
___________

* Rename the custom function with another name




Specs
_____

+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/AssertFunctionIsReserved                                                                                                                                                                                   |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP73 <ruleset-CompatibilityPHP73>`, :ref:`Deprecated <ruleset-Deprecated>` |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 1.3.9                                                                                                                                                                                                          |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                                                                                            |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Critical                                                                                                                                                                                                       |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                                                                                                  |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.2 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                                                                                                                     |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                                      |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                        |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


