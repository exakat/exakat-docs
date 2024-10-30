.. _functions-noreferencedvoid:

.. _no-referenced-void:

No Referenced Void
++++++++++++++++++

  There is no point returning a reference with a void type. This is now reported as deprecated in PHP 8.1.

.. code-block:: php
   
   <?php
   
   function &test(): void {}
   
   ?>

See also `PHP RFC: Deprecations for PHP 8.1 <https://wiki.php.net/rfc/deprecations_php_8_1>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Only+variable+references+should+be+returned+by+reference.html>`_



Connex PHP features
-------------------

  + `void <https://php-dictionary.readthedocs.io/en/latest/dictionary/void.ini.html>`_
  + `reference <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_


Suggestions
___________

* Removes the reference operator from the function definition




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NoReferencedVoid                                                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`, :ref:`Deprecated <ruleset-Deprecated>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.4                                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


