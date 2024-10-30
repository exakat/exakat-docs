.. _exceptions-unthrown:

.. _unthrown-exception:

Unthrown Exception
++++++++++++++++++

  These exceptions are defined in the code but never thrown. They are probably dead code.

Unused exceptions are code bloat, as they increase the size of the code without any purpose. They are also misleading, as other developers might come to the impression that there is a mechanism to handle the situation that the `exception <https://www.php.net/exception>`_ describe, yet they are generating a fatal `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   //This exception is defined but never used in the code.
   class myUnusedException extends \Exception {}
   
   //This exception is defined and used in the code.
   class myUsedException extends \Exception {}
   
   throw new myUsedException('I was called');
   
   ?>
Connex PHP features
-------------------

  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Suggestions
___________

* Remove the exception
* Find a place in the code to throw the exception
* Replace an existing \Exception with this more specific one




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/Unthrown                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-unthrown-exceptions <https://github.com/dseguy/clearPHP/tree/master/rules/no-unthrown-exceptions.md>`__                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


