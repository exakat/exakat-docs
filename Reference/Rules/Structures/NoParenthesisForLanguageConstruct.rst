.. _structures-noparenthesisforlanguageconstruct:

.. _no-parenthesis-for-language-construct:

No Parenthesis For Language Construct
+++++++++++++++++++++++++++++++++++++

  Some PHP language constructs, such are ``include``, ``require``, ``include_once``, ``require_once``, ``print``, ``echo`` don't need parenthesis. They accept parenthesis, but it is may lead to strange situations. 
It it better to avoid using parenthesis with ``echo``, ``print``, ``return``, ``throw``, ``yield``, ``yield from``, ``include``, ``require``, ``include_once``, ``require_once``.

.. code-block:: php
   
   <?php
   
   // This is an attempt to load 'foo.inc', or kill the script
   include('foo.inc') or die();
   // in fact, this is read by PHP as : include 1 
   // include  'foo.inc' or die();
   
   ?>

See also `ON PHP LANGUAGE CONSTRUCTS AND PARENTHESES <https://tfrommen.de/on-php-language-constructs-and-parentheses/>`_ and  `include <https://www.php.net/manual/en/function.include.php>`_.


Suggestions
___________

* Remove parenthesis




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoParenthesisForLanguageConstruct                                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | parenthesis, language-construct, return, include                                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-parenthesis-for-language-construct <https://github.com/dseguy/clearPHP/tree/master/rules/no-parenthesis-for-language-construct.md>`__                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpdocumentor-structures-noparenthesisforlanguageconstruct`, :ref:`case-phpmyadmin-structures-noparenthesisforlanguageconstruct`                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


