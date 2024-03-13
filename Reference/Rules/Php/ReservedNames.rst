.. _php-reservednames:

.. _php-keywords-as-names:

PHP Keywords As Names
+++++++++++++++++++++

  PHP has a set of reserved keywords. It is recommended not to use those keywords for names structures. 

PHP does check that a number of structures, such as classes, methods, interfaces... can't be named or called using one of the keywords. However, in a few other situations, no check are enforced. Using keywords in such situation is confusing.

.. code-block:: php
   
   <?php
   
   // This keyword is reserved since PHP 7.2
   class object {
       // _POST is used by PHP for the $_POST variable
       // This methods name is probably confusing, 
       // and may attract more than its share of attention
       function _POST() {
       
       }
   }
   
   ?>

+---------------+---------+--------+------------------------------------------------------------------------------------+
| Name          | Default | Type   | Description                                                                        |
+---------------+---------+--------+------------------------------------------------------------------------------------+
| reservedNames |         | string | Other reserved names : all in a string, comma separated.                           |
+---------------+---------+--------+------------------------------------------------------------------------------------+
| allowedNames  |         | string | PHP reserved names that can be used in the code. All in a string, comma separated. |
+---------------+---------+--------+------------------------------------------------------------------------------------+



See also `List of Keywords <https://www.php.net/manual/en/reserved.keywords.php>`_, `Predefined Classes <https://www.php.net/manual/en/reserved.classes.php>`_, `Predefined Constants <https://www.php.net/manual/en/reserved.constants.php>`_, `List of other reserved words <https://www.php.net/manual/en/reserved.other-reserved-words.php>`_ and `Predefined Variables <https://www.php.net/manual/en/reserved.variables.php>`_.


Suggestions
___________

* Rename the structure
* Choose another naming convention to avoid conflict and rename the current structures




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ReservedNames                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | reserved-name                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-churchcrm-php-reservednames`, :ref:`case-xataface-php-reservednames`                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


