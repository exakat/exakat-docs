.. _functions-usesdefaultarguments:

.. _uses-default-values:

Uses Default Values
+++++++++++++++++++

  Default values are provided to methods so as to make it convenient to use. However, with new versions, those values may change. For example, in PHP 5.4, `htmlentities() <https://www.php.net/htmlentities>`_ switched from ``Latin1`` to ``UTF-8`` default encoding.
As much as possible, it is recommended to use explicit values in those methods, so as to prevent from being surprise at a future PHP evolution. 

This analyzer tend to report a lot of false positives, including usage of `count() <https://www.php.net/count>`_. `Count() <https://www.php.net/count>`_ indeed has a second argument for recursive counts, and a default value. This may be ignored safely.

.. code-block:: php
   
   <?php
   
   $string = Eu não sou o pão;
   
   echo htmlentities($string);
   
   // PHP 5.3 : Eu n&Atilde;&pound;o sou o p&Atilde;&pound;o
   // PHP 5.4 : Eu n&atilde;o sou o p&atilde;o
   
   // Stable across versions
   echo htmlentities($string, 'UTF8');
   
   ?>

Suggestions
___________

* Mention all arguments, as much as possible




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UsesDefaultArguments                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
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


