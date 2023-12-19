.. _php-uppercasekeyword:

.. _non-lowercase-keywords:

Non-lowercase Keywords
++++++++++++++++++++++

  The usual convention is to write PHP keywords (like ``as``, ``foreach``, ``switch``, ``case``, ``break``, etc.) all in lowercase. 


.. code-block:: php
   
   <?php
   
   // usual PHP convention
   foreach($array as $element) {
       echo $element;
   }
   
   // unusual PHP conventions
   Foreach($array AS $element) {
       eCHo $element;
   }
   
   ?>


PHP understands them in lowercase, UPPERCASE or WilD Case, so there is nothing compulsory here. Although, it will look strange to many. 

Some keywords are missing from this analysis : ``extends``, ``implements``, ``as``. This is due to the internal `engine <https://www.php.net/engine>`_, which doesn't keep track of them in its AST representation.

Suggestions
___________

* Use lowercase only PHP keywords, except for constants such as __CLASS__.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UpperCaseKeyword                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Coding conventions <ruleset-Coding-conventions>`                                        |
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
| Features     | case                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


