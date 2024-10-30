.. _functions-wrongargumentnamewithphpfunction:

.. _wrong-argument-name-with-php-function:

Wrong Argument Name With PHP Function
+++++++++++++++++++++++++++++++++++++

  The name of the argument provided is not a valid parameter name for that PHP native function or method. 
This analysis may be configured with extra PHP extensions or external packages.

.. code-block:: php
   
   <?php
   
   // those are the valid names
   strcmp(string1: 'a', string2: 'b');
   
   // those are not the valid names
   strcmp(string: 'a', stringToo: 'b');
   
   ?>

See also :ref:`Unknown Parameter Name <unknown-parameter-name>`.

Connex PHP features
-------------------

  + `named-parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/named-parameter.ini.html>`_


Suggestions
___________

* Use the correct parameter name
* Remove all the parameter names from the call
* Create a relay function with the correct parameter names




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/WrongArgumentNameWithPhpFunction                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.3                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


