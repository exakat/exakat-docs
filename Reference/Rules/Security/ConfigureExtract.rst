.. _security-configureextract:

.. _configure-extract:

Configure Extract
+++++++++++++++++

  The `extract() <https://www.php.net/extract>`_ function overwrites local variables when left unconfigured.

Extract imports variables from an array into the local scope. In case of a conflict, that is when a local variable already exists, it overwrites the previous variable.

In fact, `extract() <https://www.php.net/extract>`_ may be configured to handle the situation differently : it may skip the conflicting variable, prefix it, prefix it only if it exists, only import overwriting variables... It may also import them as references to the original values.

This analysis reports `extract() <https://www.php.net/extract>`_ when it is not configured explicitly. If overwriting is the intended objective, it is not reported.


.. code-block:: php
   
   <?php
   
   // ignore overwriting variables
   extract($array, EXTR_SKIP);
   
   // prefix all variables explicitly variables with 'php_'
   extract($array, EXTR_PREFIX_ALL, 'php_');
   
   // overwrites explicitly variables
   extract($array, EXTR_OVERWRITE);
   
   // overwrites implicitely variables : do we really want that? 
   extract($array, EXTR_OVERWRITE);
   
   ?>


Always avoid using `extract() <https://www.php.net/extract>`_ on untrusted sources, such as ``$_GET``, ``$_POST``, ``$_FILES``, or even databases records.

See also `extract <https://www.php.net/extract>`_.


Suggestions
___________

* Always use the second argument of extract(), and avoid using ``EXTR_OVERWRITE``




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/ConfigureExtract                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Security <ruleset-Security>`                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | extract, variable                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-security-configureextract`, :ref:`case-dolibarr-security-configureextract`                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


