.. _performances-substrfirst:

.. _substring-first:

Substring First
+++++++++++++++

  Always start by reducing a string before applying some transformation on it. The shorter string will be processed faster. 


.. code-block:: php
   
   <?php
   
   // fast version
   $result = strtolower(substr($string, $offset, $length));
   
   // slower version
   $result = substr(strtolower($string), $offset, $length);
   ?>


The gain produced here is greater with longer strings, or greater reductions. They may also be used in loops. This is a micro-optimisation when used on short strings and single string reductions.

This works with any reduction function instead of `substr() <https://www.php.net/substr>`_, like `trim() <https://www.php.net/trim>`_, `iconv() <https://www.php.net/iconv>`_, etc.

Suggestions
___________

* Always reduce the string first, then apply some transformation




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/SubstrFirst                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.1                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | declare                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-spip-performances-substrfirst`, :ref:`case-prestashop-performances-substrfirst`                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------+


