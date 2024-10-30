.. _php-castunsetusage:

.. _cast-unset-usage:

Cast Unset Usage
++++++++++++++++

  Usage of the `(unset)` cast operator was removed. The operator was deprecated since PHP 7.2.0.

.. code-block:: php
   
   <?php
   
   $a = 1;
   (unset) $a;
   
   // functioncall is OK
   unset($a);
   
   ?>

See also `Unset casting <https://www.php.net/manual/en/language.types.null.php#language.types.null.casting>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/The+%28unset%29+cast+is+no+longer+supported+.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/The+%28unset%29+cast+is+deprecated.html>`_



Connex PHP features
-------------------

  + `cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_
  + `unset <https://php-dictionary.readthedocs.io/en/latest/dictionary/unset.ini.html>`_


Suggestions
___________

* Replace `(unset)` with a call to unset().
* Remove the unset call altogether.
* Set the value to NULL.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CastUnsetUsage                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.8                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


