.. _php-sethandlers:

.. _php-handlers-usage:

PHP Handlers Usage
++++++++++++++++++

  PHP has a number of handlers that may be replaced by customized code : session, shutdown, `error <https://www.php.net/error>`_, `exception <https://www.php.net/exception>`_. They are noted here.

The example is adapted from the PHP documentation of `set_error_handler() <https://www.php.net/set_error_handler>`_.

.. code-block:: php
   
   <?php
   // error handler function
   function myErrorHandler($errno, $errstr, $errfile, $errline)
   {
       if (!(error_reporting() & $errno)) {
           // This error code is not included in error_reporting, so let it fall
           // through to the standard PHP error handler
           return false;
       }
   
       switch ($errno) {
       case E_USER_ERROR:
           echo '<b>My ERROR</b> [$errno] $errstr<br />'.PHP_EOL;
           echo '  Fatal error on line '.$errline.' in file .'$errfile;
           echo ', PHP ' . PHP_VERSION . ' (' . PHP_OS . ')<br />'.PHP_EOL;
           echo 'Aborting...<br />'.PHP_EOL;
           exit(1);
           break;
   
       case E_USER_WARNING:
           echo '<b>My WARNING</b> ['.$errno.'] '.$errstr.'<br />'.PHP_EOL;
           break;
   
       case E_USER_NOTICE:
           echo '<b>My NOTICE</b> ['.$errno.'] '.$errstr.'<br />'.PHP_EOL;
           break;
   
       default:
           echo 'Unknown error type: ['.$errno.'] $errstr<br />'.PHP_EOL;
           break;
       }
   
       /* Don't execute PHP internal error handler */
       return true;
   }
   
   
   // set to the user defined error handler
   $old_error_handler = set_error_handler("myErrorHandler");
   
   ?>

See also `set_error_handler <http://www.php.net/set_error_handler>`_.

Connex PHP features
-------------------

  + `handler <https://php-dictionary.readthedocs.io/en/latest/dictionary/handler.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/SetHandlers                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


