.. _structures-simplepreg:

.. _simplify-regex:

Simplify Regex
++++++++++++++

  Avoid using regex when the searched string or the replacement are simple enough.

PRCE regex are a powerful way to search inside strings, but they also come at the price of performance. When the query is simple enough, try using `strpos() <https://www.php.net/strpos>`_ or `stripos() <https://www.php.net/stripos>`_ instead.

.. code-block:: php
   
   <?php
   
   // simple preg calls
   if (preg_match('/a/', $string))  {}
   if (preg_match('/b/i', $string)) {} // case insensitive
   
   // light replacements
   if( strpos('a', $string)) {}
   if( stripos('b', $string)) {}       // case insensitive
   
   ?>
Connex PHP features
-------------------

  + `regex <https://php-dictionary.readthedocs.io/en/latest/dictionary/regex.ini.html>`_


Suggestions
___________

* Use str_replace(), strtr() or even strpos()




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SimplePreg                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-structures-simplepreg`, :ref:`case-openconf-structures-simplepreg`                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


