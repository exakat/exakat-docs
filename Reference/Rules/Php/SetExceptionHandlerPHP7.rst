.. _php-setexceptionhandlerphp7:

.. _set\_exception\_handler()-warning:

set_exception_handler() Warning
+++++++++++++++++++++++++++++++

  The `set_exception_handler() <https://www.php.net/set_exception_handler>`_ callable function has to be adapted to PHP 7 : ``Exception`` is not the right typehint, it is now ``Throwable``. 

When in doubt about backward compatibility, just drop the typehint. Otherwise, use ``Throwable``.


.. code-block:: php
   
   <?php
   
   // PHP 5.6- typehint 
   class foo { function bar(\Exception $e) {} }
   
   // PHP 7+ typehint 
   class foo { function bar(Throwable $e) {} }
   
   // PHP 5 and PHP 7 compatible typehint (note : there is none)
   class foo { function bar($e) {} }
   
   set_exception_handler(foo);
   
   ?>

See also Drop the type and Use Throwable type.


Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/SetExceptionHandlerPHP7                                                                                                          |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Features         | error-handler                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


