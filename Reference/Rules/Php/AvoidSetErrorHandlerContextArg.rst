.. _php-avoidseterrorhandlercontextarg:

.. _avoid-set\_error\_handler-$context-argument:

Avoid set_error_handler $context Argument
+++++++++++++++++++++++++++++++++++++++++

  Avoid configuring `set_error_handler() <https://www.php.net/set_error_handler>`_ with a method that accepts 5 arguments. The last argument, ``$errcontext``, is deprecated since PHP 7.2, and will be removed later.

.. code-block:: php
   
   <?php
   
   // setting error_handler with an incorrect closure
   set_error_handler(function($errno, $errstr, $errfile, $errline) {});
   
   // setting error_handler with an incorrect closure
   set_error_handler(function($errno, $errstr, $errfile, $errline, $errcontext) {});
   
   ?>

See also set_error_handler().

Connex PHP features
-------------------

  + `error-handler <https://php-dictionary.readthedocs.io/en/latest/dictionary/error-handler.ini.html>`_


Suggestions
___________

* Remove the 6th argument of registered handlers.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/AvoidSetErrorHandlerContextArg                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-shopware-php-avoidseterrorhandlercontextarg`, :ref:`case-vanilla-php-avoidseterrorhandlercontextarg`                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


