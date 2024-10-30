.. _arrays-floatconversionasindex:

.. _float-conversion-as-index:

Float Conversion As Index
+++++++++++++++++++++++++

  Only integers and strings are possible types when used for array index. Until PHP 8.1, floats were converted to integer by truncation. Since PHP 8.1, a deprecated message is emitted.

 The implicit conversion of float to int which leads to a loss in precision is now deprecated. This affects array keys, int type declarations in coercive mode, and operators working on integers.

.. code-block:: php
   
   <?php
   $a = [];
   $a[15.5]; // deprecated, as key value loses the 0.5 component
   $a[15.0]; // ok, as 15.0 == 15
   ?>

See also `Implicit incompatible float to int conversions <https://www.php.net/manual/en/migration81.deprecated.php#migration81.deprecated.core.implicit-float-conversion>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Implicit+conversion+from+float+3.141592653589793+to+int+loses+precision.html>`_



Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Use the cast operator (string) to convert the floats into strings. The reverse cast is most often possible.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/FloatConversionAsIndex                                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.1                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


