.. _php-scalararenotarrays:

.. _scalar-are-not-arrays:

Scalar Are Not Arrays
+++++++++++++++++++++

  It is wrong to use a scalar as an array, a Warning is emitted. PHP 7.4 emits a Warning in such situations.
Typehinted argument with a scalar are reported by this analysis. Also, nullable arguments, both with typehint and return type hint.

.. code-block:: php
   
   <?php
   
   // Here, $x may be null, and in that case, the echo will fail.
   function foo(?A $x) { 
       echo $x[2]; 
   }
   
   ?>

See also `E_WARNING for invalid container read array-access <https://wiki.php.net/rfc/notice-for-non-valid-array-container>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Trying+to+access+array+offset+on+value+of+type+null.html>`_



Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_
  + `array-object <https://php-dictionary.readthedocs.io/en/latest/dictionary/array-object.ini.html>`_


Suggestions
___________

* Update type hints to avoid scalar values
* Remove the array syntax in the code using the results
* Cast to string type, so the array notation is accessible




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ScalarAreNotArrays                                                                                                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.0                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


