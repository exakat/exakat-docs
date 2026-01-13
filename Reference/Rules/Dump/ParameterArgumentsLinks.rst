.. _dump-parameterargumentslinks:

.. _links-between-parameter-and-argument:

Links Between Parameter And Argument
++++++++++++++++++++++++++++++++++++

  Collect various stats about arguments and parameter usage. 

A parameter is one slot in the method definition. An argument is a slot in the method call. Both are linked by the method and their respective position in the argument list.

+ Total number of argument usage, linked to a parameter : this excludes arguments from external libraries and native PHP functions. For reference.
+ Number of identical parameter : cases where argument and parameter have the same name. 
+ Number of different parameter : cases where argument and parameter have the different name. 
+ Number of expression argument : cases where argument is an expression
+ Number of constant argument : cases where the argument is a constant

.. code-block:: php
   
   <?php
   
   function foo($a, $b) {
       // some code
   }
   
   // $a is the same as the parameter
   // $c is different from the paramter $b
   foo($a, $c);
   
   const C = 1;
   
   // Foo is called with a constant (1rst argument)
   // Foo is called with a expression (2nd argument)
   foo(C, 1+3);
   
   ?>
Connex PHP features
-------------------

  + `parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/parameter.ini.html>`_
  + `argument <https://php-dictionary.readthedocs.io/en/latest/dictionary/argument.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/ParameterArgumentsLinks                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.6                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


