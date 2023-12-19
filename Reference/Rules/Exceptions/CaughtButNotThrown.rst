.. _exceptions-caughtbutnotthrown:

.. _undefined-caught-exceptions:

Undefined Caught Exceptions
+++++++++++++++++++++++++++

  Those are exceptions that are caught in the code, but are not defined in the application. 

They may be externally defined, such as in core PHP, extensions or libraries. Make sure those exceptions are useful to your application : otherwise, they are dead code.


.. code-block:: php
   
   <?php
   
   try {
       library_function($some, $args);
       
   } catch (LibraryException $e) {
       // This exception is not defined, and probably belongs to Library
       print "Library failed\n";
   
   } catch (OtherLibraryException $e) {
       // This exception is not defined, and probably do not belongs to this code
       print "Library failed\n";
   
   } catch (\Exception $e) {
       // This exception is a PHP standard exception
       print "Something went wrong, but not at Libary level\n";
   }
   
   ?>

Suggestions
___________

* Remove the catch clause, as it is dead code
* Make sure the exception is thrown by the underlying code




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/CaughtButNotThrown                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Dead code <ruleset-Dead-code>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | exception, predefined-exception                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


