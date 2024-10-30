.. _php-reservedmatchkeyword:

.. _reserved-match-keyword:

Reserved Match Keyword
++++++++++++++++++++++

  ``match`` is a new instruction in PHP 8.0. 

For that, it becomes a reserved keyword, and cannot be used in various situations: type, class, function, global constant name.

.. code-block:: php
   
   <?php
   
   // Match as a standalone keyword is not possible
   use X as Match;
   
   // No more use as a type
   function foo(match $a ) : match {}
   $a instanceof match; 
   
   // No use as method name
   match(a, 4) ;
   
   // Match in a Fully qualified name is OK
   b\match ;
   
   // Match as a property name or a class constant is OK
   $match->match;
   C::MATCH;
   
   // Match as a method is OK
   $method->match();
   $static::match();
   
   ?>

See also `Match expression V2 <https://wiki.php.net/rfc/match_expression_v2>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/syntax+error%2C+unexpected+%27match%27.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/syntax+error%2C+unexpected+%27%2C%27.html>`_



Connex PHP features
-------------------

  + `match <https://php-dictionary.readthedocs.io/en/latest/dictionary/match.ini.html>`_


Suggestions
___________

* Change the name from Match to something else.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ReservedMatchKeyword                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`uses-php-8-match()`                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


