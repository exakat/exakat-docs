.. _exceptions-convertedexceptions:

.. _converted-exceptions:

Converted Exceptions
++++++++++++++++++++

  Converted exceptions is when an `exception <https://www.php.net/exception>`_ is caught, then immediately converted into another one and thrown again.

Sometimes, extra operations take place, such as logging or `error <https://www.php.net/error>`_ couting.

.. code-block:: php
   
   <?php
   
   try {
   	doSomething();
   } catch (MyException $e) {
   	log($e->getMessage());
   	throw new BadRequestException();
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/ConvertedExceptions                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | exception, try                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


