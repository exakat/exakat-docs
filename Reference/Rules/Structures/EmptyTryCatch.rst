.. _structures-emptytrycatch:

.. _empty-try-catch:

Empty Try Catch
+++++++++++++++

  The code does try, then catch errors but do no act upon the `error <https://www.php.net/error>`_. 



At worst, the `error <https://www.php.net/error>`_ should be logged, so as to measure the actual usage of the catch expression.

``catch( `Exception <https://www.php.net/exception>`_ $e)`` (PHP 5) or ``catch(`Throwable <https://www.php.net/manual/en/class.`throwable <https://www.php.net/throwable>`_.php>`_ $e)`` with empty catch block should be banned. They ignore any `error <https://www.php.net/error>`_ and proceed as if nothing happened. At worst, the event should be logged for future analysis.

.. code-block:: php
   
   <?php
   
   try { 
       doSomething();
   } catch (Throwable $e) {
       // ignore this
   }
   
   ?>

See also `Empty Catch Clause <http://wiki.c2.com/?EmptyCatchClause>`_.


Suggestions
___________

* Add some logging in the catch
* Add a comment to mention why the catch is empty
* Change the exception, chain it and throw again




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/EmptyTryCatch                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
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
| Features     | try                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-livezilla-structures-emptytrycatch`, :ref:`case-mautic-structures-emptytrycatch`                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


