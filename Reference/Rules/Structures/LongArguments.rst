.. _structures-longarguments:

.. _long-arguments:

Long Arguments
++++++++++++++

.. meta::
	:description:
		Long Arguments: Long arguments should be put in variable, to preserve readability.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Long Arguments
	:twitter:description: Long Arguments: Long arguments should be put in variable, to preserve readability
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Long Arguments
	:og:type: article
	:og:description: Long arguments should be put in variable, to preserve readability
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Long Arguments.html
	:og:locale: en
Long arguments should be put in variable, to preserve readability. 

When literal arguments are too long, they `break <https://www.php.net/manual/en/control-structures.break.php>`_ the hosting structure by moving the next argument too far on the right. Whenever possible, long arguments should be set in a local variable to keep the readability.
Literal strings and heredoc strings, including variables, that are over 50 chars longs are reported here.

.. code-block:: php
   
   <?php
   
   // Now the call to foo() is easier to read.
   $reallyBigNumber = <<<BIGNUMBER
   123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890
   BIGNUMBER
   foo($reallyBigNumber, 2, '12345678901234567890123456789012345678901234567890');
   
   // where are the next arguments ? 
   foo('123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890', 2, '123456789012345678901234567890123456789012345678901234567890');
   
   // This is still difficult to read
   foo(<<<BIGNUMBER
   123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890
   BIGNUMBER
   , 2, '123456789012345678901234567890123456789012345678901234567890');
   
   ?>

+-------------+---------+---------+---------------------------------------------------------------------------+
| Name        | Default | Type    | Description                                                               |
+-------------+---------+---------+---------------------------------------------------------------------------+
| codeTooLong | 100     | integer | Minimum size of a functioncall or a methodcall to be considered too long. |
+-------------+---------+---------+---------------------------------------------------------------------------+


Connex PHP features
-------------------

  + `argument <https://php-dictionary.readthedocs.io/en/latest/dictionary/argument.ini.html>`_
  + `readability <https://php-dictionary.readthedocs.io/en/latest/dictionary/readability.ini.html>`_


Suggestions
___________

* Put the long arguments in a separate variable, and use the variable in the second expression, reducing its total length 




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/LongArguments                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-cleverstyle-structures-longarguments`, :ref:`case-contao-structures-longarguments`                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


