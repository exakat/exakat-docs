.. _constants-caseinsensitiveconstants:

.. _case-insensitive-constants:

Case Insensitive Constants
++++++++++++++++++++++++++

  PHP constants used to be able to be case insensitive, when defined with `define() <https://www.php.net/define>`_ and the third argument.

This feature is deprecated since PHP 7.3 and is removed since PHP 8.0.

.. code-block:: php
   
   <?php
   
   // case sensitive
   define('A', 1);
   
   // case insensitive
   define('B', 1, true);
   
   echo A;
   // This is not possible
   //echo a;
   
   // both possible
   echo B;
   echo b;
   
   ?>

See also `define <https://www.php.net/define>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/define%28%29%3A+Declaration+of+case-insensitive+constants+is+deprecated.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/Argument+%233+%28%24case_insensitive%29+is+ignored+since+declaration+of+case-insensitive+constants+is+no+longer+supported.html>`_



Connex PHP features
-------------------

  + `dynamic-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-constant.ini.html>`_
  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/CaseInsensitiveConstants                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP73 <ruleset-CompatibilityPHP73>`, :ref:`Deprecated <ruleset-Deprecated>`      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.9                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


