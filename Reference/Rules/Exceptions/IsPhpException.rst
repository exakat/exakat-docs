.. _exceptions-isphpexception:

.. _php-exception:

PHP Exception
+++++++++++++

  Mark an `exception <https://www.php.net/exception>`_ as a native `exception <https://www.php.net/exception>`_. They may come from PHP standard distribution or an extension.

.. code-block:: php
   
   <?php
   
   // From the native set
   $a = new LogicException('Logic error');
   throw $a;
   
   // From an extension
   throw new ZookeeperException('Zookeeper error');
   
   ?>

See also `Exceptions <https://www.php.net/manual/en/language.exceptions.php>`_.

Connex PHP features
-------------------

  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/IsPhpException                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


