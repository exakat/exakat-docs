.. _constants-dynamiccreation:

.. _constant-dynamic-creation:

Constant Dynamic Creation
+++++++++++++++++++++++++

  Registering constant with dynamic values. Dynamic values include values read in external sources (files, databases, remote API, `... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_ ), random sources (time, `rand() <https://www.php.net/rand>`_, `...) <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_

Dynamic constants are not possible with the ``const`` keyword, though `static <https://www.php.net/manual/en/language.oop5.static.php>`_ constant expression allows for a good range of combinations, including conditions.

.. code-block:: php
   
   <?php
   
   $a = range(0, 4);
   foreach($array as $i) {
       define("A$i", $i);
       define("N$i", true);
   }
   
   define("C", 5);
   
   ?>

See also `PHP Constants <https://www.php.net/manual/en/language.constants.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/DynamicCreation                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.7                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | constant                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


