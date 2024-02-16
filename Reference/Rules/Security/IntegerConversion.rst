.. _security-integerconversion:

.. _insecure-integer-validation:

Insecure Integer Validation
+++++++++++++++++++++++++++

  Comparing incoming variables to integer may lead to injection.

When comparing a variable to an integer, PHP applies type juggling, and transform the variable in an integer too. When the value converts smoothly to an integer, this means the validation may pass and yet, the value may carry an injection.


.. code-block:: php
   
   <?php
   
   // This is safe : 
   if ($_GET['x'] === "2") {
       echo $_GET['x'];
   }
   
   // Using (int) for validation and for display
   if ((int) $_GET['x'] === 2) {
       echo (int) $_GET['x'];
   }
   
   // This is an injection
   // '2 <script>' == 2, then echo will make the injection
   if ($_GET['x'] == 2) {
       echo $_GET['x'];
   }
   
   // This is unsafe, as $_GET['x']  is tested as an integer, but echo'ed raw
   if ((int) $_GET['x'] === 2) {
       echo $_GET['x'];
   }
   
   ?>


This analysis spots situations where an incoming value is compared to an integer. The usage of the validated value is not analyzed further.

See also `Type Juggling Authentication Bypass Vulnerability in CMS Made Simple <https://www.netsparker.com/blog/web-security/type-juggling-authentication-bypass-cms-made-simple/>`_, `PHP STRING COMPARISON VULNERABILITIES <https://hydrasky.com/network-security/php-string-comparison-vulnerabilities/>`_ and `PHP Magic Tricks: Type Juggling <https://www.owasp.org/images/6/6b/PHPMagicTricks-TypeJuggling.pdf>`_.


Suggestions
___________

* Add the typecasting to all read access to the incoming variable
* Add the typecasting when writing the incoming value to a local variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/IntegerConversion                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Security <ruleset-Security>`                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | validation                                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


