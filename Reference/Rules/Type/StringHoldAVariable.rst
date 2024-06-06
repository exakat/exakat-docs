.. _type-stringholdavariable:

.. _string-may-hold-a-variable:

String May Hold A Variable
++++++++++++++++++++++++++

  Strings that contains a variable, yet are not interpolated. 

Single quotes and Nowdoc syntax may include $ signs. They are treated as literals, and not replaced with a variable value. 

However, there are some potential variables in those strings, making it possible for an `error <https://www.php.net/error>`_ : the variable was forgotten and will be published as such. It is worth checking the content and make sure those strings are not variables.

.. code-block:: php
   
   <?php
   
   $a = 2;
   
   // Explicit variable, but literal effect is needed
   echo '$a is '.$a;
   
   // One of the variable has been forgotten
   echo '$a is $a';
   
   // $CAD is not a variable, rather a currency unit
   $total = 12;
   echo $total.' $CAD';
   
   // $CAD is not a variable, rather a currency unit
   $total = 12;
   
   // Here, $total has been forgotten
   echo <<<'TEXT'
   $total $CAD
   TEXT;
   
   ?>

Suggestions
___________

* Check if the variable is really a variable
* Turn the string into an interpolated string (double quote, heredoc, concatenation)




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/StringHoldAVariable                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | variable, interpolation                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


