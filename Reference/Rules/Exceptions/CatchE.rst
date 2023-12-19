.. _exceptions-catche:

.. _caught-variable:

Caught Variable
+++++++++++++++

  Catch clauses require an `exception <https://www.php.net/exception>`_ and a variable name. Often, the variable name is the same, `$e`, as learnt from the manual.

There seems to be a choice that is not enforced : one form is dominant, (> 90%) while the others are rare. 

The analyzed code has less than 10% of one of the three : for consistency reasons, it is recommended to make them all the same. 


.. code-block:: php
   
   <?php
   
   try {
       // do Something()
   }
   catch (MyException1 $e)       { $log->log($e->getMessage();}
   catch (MyException2 $e)       { $log->log($e->getMessage();}
   catch (MyException3 $e)       { $log->log($e->getMessage();}
   catch (MyException4 $e)       { $log->log($e->getMessage();}
   catch (MyException5 $e)       { $log->log($e->getMessage();}
   catch (MyException6 $e)       { $log->log($e->getMessage();}
   catch (MyException7 $e)       { $log->log($e->getMessage();}
   catch (MyException8 $e)       { $log->log($e->getMessage();}
   catch (MyException9 $e)       { $log->log($e->getMessage();}
   catch (MyException10 $e)      { $log->log($e->getMessage();}
   catch (\RuntimeException $e)  { $log->log($e->getMessage();}
   catch (\Error $error)         { $log->log($error->getMessage();}
   catch (\Exception $exception) { $log->log($exception->getMessage();}
   ?>

Suggestions
___________

* Make all caught constant consistent, and avoid using them for something else




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/CatchE                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | exception                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


