.. _php-directivename:

.. _unknown-directive-name:

Unknown Directive Name
++++++++++++++++++++++

  Unknown directives names used in the code. 

The following list has directive mentioned in the code, that are not known from PHP or any extension. If this is due to a mistake, the directive must be fixed to be actually useful.

.. code-block:: php
   
   <?php
   
   // non-existing directive
   $reporting_error = ini_get('reporting_error');
   $error_reporting = ini_get('error_reproting'); // Note the inversion
   if (ini_set('dump_globals')) {
       // doSomething()
   }
   
   // Correct directives
   $error_reporting = ini_get('reporting_error');
   if (ini_set('xdebug.dump_globals')) {
       // doSomething()
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/DirectiveName                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | directive                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


