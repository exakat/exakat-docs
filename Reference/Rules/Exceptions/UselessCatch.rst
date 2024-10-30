.. _exceptions-uselesscatch:

.. _useless-catch:

Useless Catch
+++++++++++++

  A catch clause should handle the `exception <https://www.php.net/exception>`_ by doing something. 

Among the task of a catch clause : log the `exception <https://www.php.net/exception>`_, clean any mess that was introduced, fail graciously.

In particular, a return inside a catch clause might short-circuit the commands laid after the try/catch block. 

It is also a sign that there is no `error <https://www.php.net/error>`_, and the `exception <https://www.php.net/exception>`_ shall be handled with a preemptive check, rather than an `error <https://www.php.net/error>`_ review.


.. code-block:: php
   
   <?php
   
   function foo($a) {
       try {
           $b = doSomething($a);
       } catch (Throwable $e) {
           // No log of the exception : no one knows it happened.
           
           // return immediately ? 
           return false;
       }
       
       $b->complete();
       
       return $b;
   }
   
   ?>

See also `Exceptions <https://www.php.net/manual/en/language.exceptions.php>`_ and `Best practices for PHP exception handling <https://www.moxio.com/blog/34/best-practices-for-php-exception-handling>`_.

Connex PHP features
-------------------

  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_
  + `catch <https://php-dictionary.readthedocs.io/en/latest/dictionary/catch.ini.html>`_


Suggestions
___________

* Add a log call to the catch block.
* Handle correctly the exception.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/UselessCatch                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-exceptions-uselesscatch`, :ref:`case-prestashop-exceptions-uselesscatch`                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


