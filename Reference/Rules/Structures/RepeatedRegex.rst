.. _structures-repeatedregex:

.. _repeated-regex:

Repeated Regex
++++++++++++++

  Repeated regex should be centralized. 

When a regex is repeatedly used in the code, it is getting harder to update. 
Regex that are repeated at least once (aka, used twice or more) are reported. Regex that are dynamically build are not reported.

.. code-block:: php
   
   <?php
   
   // Regex used several times, at least twice.
   preg_match('/^abc_|^square$/i', $_GET['x']);
   
   //.......
   
   preg_match('/^abc_|^square$/i', $row['name']);
   
   // This regex is dynamically built, so it is not reported.
   preg_match('/^circle|^'.$x.'$/i', $string);
   
   // This regex is used once, so it is not reported.
   preg_match('/^circle|^square$/i', $string);
   
   ?>
Connex PHP features
-------------------

  + `regex <https://php-dictionary.readthedocs.io/en/latest/dictionary/regex.ini.html>`_


Suggestions
___________

* Create a central library of regex
* Use the regex inventory to spot other regex that are close, and should be identical.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/RepeatedRegex                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.9                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-vanilla-structures-repeatedregex`, :ref:`case-tikiwiki-structures-repeatedregex`                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


