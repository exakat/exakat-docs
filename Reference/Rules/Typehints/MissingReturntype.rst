.. _typehints-missingreturntype:

.. _missing-some-returntype:

Missing Some Returntype
+++++++++++++++++++++++

  The specified typehints are not compatible with the returned values. 

The code of the method may return other types, which are not specified and will lead to a PHP fatal `error <https://www.php.net/error>`_. It is the case for insufficient typehints, when a typehint is missing, or inconsistent typehints, when the method returns varied types. 


.. code-block:: php
   
   <?php
   
   // correct return typehint
   function fooSN() : ?string  {
       return shell_exec('ls -hla');
   }
   
   // insufficient return typehint
   // shell_exec() may return null or string. Here, only string in specified for fooS, and that may lead to a Fatal error
   function fooS() : string  {
       return shell_exec('ls -hla');
   }
   
   // inconsistent return typehint
   function bar() : int {
       return rand(0, 10) ? 1 : "b";
   }
   
   ?>


The analysis reports a method when it finds other return types than the one expected. In the case of multiple typehints, as for the last example, the PHP code may require an upgrade to PHP 8.0.

Suggestions
___________

* Update the typehint to accept more types
* Update the code of the method to fit the expected returntype




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/MissingReturntype                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.7                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | return-typehint                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


