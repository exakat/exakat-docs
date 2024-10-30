.. _structures-nochangeincomingvariables:

.. _don't-change-incomings:

Don't Change Incomings
++++++++++++++++++++++

  PHP hands over a lot of information using special variables like `$_GET <https://www.php.net/manual/en/reserved.variables.get.php>`_, `$_POST <https://www.php.net/manual/en/reserved.variables.post.php>`_, etc... Modifying those variables and those values inside variables means that the original content is lost, while it will still look like raw data, and, as such, will be untrustworthy.
It is recommended to put the modified values in another variable, and keep the original one intact.

.. code-block:: php
   
   <?php
   
   // filtering and keeping the incoming value. 
   $_DATA'id'] = (int) $_GET['id'];
   
   // filtering and changing the incoming value. 
   $_GET['id'] = strtolower($_GET['id']);
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Cannot+re-assign+auto-global+variable.html>`_



Connex PHP features
-------------------

  + `incoming-data <https://php-dictionary.readthedocs.io/en/latest/dictionary/incoming-data.ini.html>`_
  + `outgoing-data <https://php-dictionary.readthedocs.io/en/latest/dictionary/outgoing-data.ini.html>`_


Suggestions
___________

* Set the value to another variable and apply modifications to that variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoChangeIncomingVariables                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


