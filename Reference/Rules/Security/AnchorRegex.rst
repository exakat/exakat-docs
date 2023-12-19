.. _security-anchorregex:

.. _always-anchor-regex:

Always Anchor Regex
+++++++++++++++++++

  Unanchored regex finds the requested pattern, and leaves room for malicious content. 

Without ``^`` and ``$``, the regex searches for any pattern that satisfies the criteria, leaving any unused part of the string available for arbitrary content. It is recommended to use both anchor


.. code-block:: php
   
   <?php
   
   $birthday = getSomeDate($_GET);
   
   // Permissive version : $birthday = '1970-01-01<script>xss();</script>';
   if (!preg_match('/\d{4}-\d{2}-\d{2}/', $birthday) {
       error('Wrong data format for your birthday!');
   }
   
   // Restrictive version : $birthday = '1970-01-01';
   if (!preg_match('/^\d{4}-\d{2}-\d{2}$/', $birthday) {
       error('Wrong data format for your birthday!');
   }
   
   echo 'Your birthday is on '.$birthday;
   
   ?>


Note that $ may be a line ending, still leaving room after it for injection.


.. code-block:: php
   
   <?php
   
   $birthday = '1970-01-01'.PHP_EOL.'<script>xss();</script>';
   
   ?>


This analysis reports false positive when the regex is used to search a pattern in a much larger string. Check if this rule doesn't apply, though.

See also `CWE-625: Permissive Regular Expression <https://cwe.mitre.org/data/definitions/625.html>`_.


Suggestions
___________

* Add an anchor to the beginning and ending of the string




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/AnchorRegex                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Security <ruleset-Security>`                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.15                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | regex                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


