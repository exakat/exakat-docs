.. _php-deprecatedollarcurly:

.. _dollar-curly-interpolation-is-deprecated:

Dollar Curly Interpolation Is Deprecated
++++++++++++++++++++++++++++++++++++++++

  Among the different variable interpolation is strings, ```` is deprecated. It is made obsolete in PHP 8.2, and should disappear in PHP 9.0.

There are still several interpolation ways : variables, array elements (one index-level) and curly brackets. It is also possible to use string concatenation. 


.. code-block:: php
   
   <?php
   
   $a = 'a';
   $a2 = 'surprise!';
   
   $b = "\\$\\{$a . 2}\"; 
   
   echo $b;
   // display 'surprise!'
   
   ?>

See also https://wiki.php.net/rfc/deprecate_dollar_brace_string_interpolation.


Suggestions
___________

* Use another interpolation style
* Use string concatenation
* Use a templating engine
* Use string replacement tool, such as str_replace()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/DeprecateDollarCurly                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.2 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | string, string-interpolation                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


