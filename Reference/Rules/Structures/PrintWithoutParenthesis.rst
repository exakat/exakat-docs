.. _structures-printwithoutparenthesis:

.. _avoid-parenthesis-with-language-construct:

Avoid Parenthesis With Language Construct
+++++++++++++++++++++++++++++++++++++++++

  Avoid Parenthesis for language construct. Languages constructs are a few PHP native elements, that looks like functions but are not. 

Among other distinction, those elements cannot be directly used as variable function call, and they may be used with or without parenthesis.


.. code-block:: php
   
   <?php
   
   // normal usage of include
   include 'file.php';
   
   // This looks like a function and is not
   include('file2.php');
   
   ?>


The usage of parenthesis actually give some feeling of comfort, it won't prevent PHP from combining those argument with any later operators, leading to unexpected results.

Even if most of the time, usage of parenthesis is legit, it is recommended to avoid them.

Suggestions
___________

* Remove the parenthesis




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/PrintWithoutParenthesis                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
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
| Features     | language-construct                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


