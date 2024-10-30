.. _classes-immutablesignature:

.. _immutable-signature:

Immutable Signature
+++++++++++++++++++

  Overwrites makes refactoring a method signature difficult. PHP enforces compatible signature, by checking if arguments have the same type, reference and default values.

In PHP 7.3, typehint had to be the same, or dropped. In PHP 7.4, typehint may be contravariant (arguments), or covariant (returntype). 

This analysis may be configured with ``maxOverwrite``. By default, a minimum of 8 overwritten methods is considered difficult to update.
When refactoring a method, all the related methodcall may have to be updated too. Adding a type, a default value, or a new argument with default value won't affect the calls, but only the definitions. Otherwise, calls will also have to be updated.

IDE may help with signature refactoring, such as `Refactoring code <https://www.jetbrains.com/help/phpstorm/refactoring-source-code.html>`_.

.. code-block:: php
   
   <?php
   
   // Changing any of the four foo() method signature will trigger a PHP warning
   class a {
       function foo($a) {}
   }
   
   class ab1 extends a {
       // four foo() methods have to be refactored at the same time!
       function foo($ab1) {}
   }
   
   class ab2 extends a {
       function foo($ab2) {}
   }
   
   class ab3 extends ab1 {
       function foo($abc1) {}
   }
   
   ?>

+--------------+---------+---------+-------------------------------------------------------------------------------------------------------+
| Name         | Default | Type    | Description                                                                                           |
+--------------+---------+---------+-------------------------------------------------------------------------------------------------------+
| maxOverwrite | 8       | integer | Minimal number of method overwrite to consider that any refactor on the method signature is now hard. |
+--------------+---------+---------+-------------------------------------------------------------------------------------------------------+



See also `Covariance and contravariance (computer science) <https://en.wikipedia.org/wiki/Covariance_and_contravariance_(computer_science)>`_ and `extends <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.extends>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Declaration+of+a%3A%3Afoo%28%24a%29+should+be+compatible+with+ab1%3A%3Afoo%28%24a%29.html>`_



Connex PHP features
-------------------

  + `overwrite <https://php-dictionary.readthedocs.io/en/latest/dictionary/overwrite.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ImmutableSignature                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


