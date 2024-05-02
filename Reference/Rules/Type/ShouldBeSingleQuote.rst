.. _type-shouldbesinglequote:

.. _should-be-single-quote:

Should Be Single Quote
++++++++++++++++++++++

  Use single quote for simple strings.

`Static <https://www.php.net/manual/en/language.oop5.static.php>`_ content inside a string, that has no single quotes nor escape sequence (such as \n or \t), should be using single quote delimiter, instead of double quote. 
If you have too many of them, don't loose your time switching them all. If you have a few of them, it may be good for consistence.

.. code-block:: php
   
   <?php
   
   $a = "abc";
   
   // This one is using a special sequence
   $b = "cde\n";
   
   // This one is using two special sequences
   $b = "\x03\u{1F418}";
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/ShouldBeSingleQuote                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Coding conventions <ruleset-Coding-conventions>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | double-quote, single-quote                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-double-quote <https://github.com/dseguy/clearPHP/tree/master/rules/no-double-quote.md>`__                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


