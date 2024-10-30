.. _php-exitnoarg:

.. _exit-without-argument:

Exit Without Argument
+++++++++++++++++++++

  This rule reports usage of `die <https://www.php.net/die>`_ and `exit <https://www.www.php.net/exit>`_ without arguments, nor parenthesis. These commands are not functions, and are allowed to be used without parenthesis: by default, they use the 0 status.

.. code-block:: php
   
   <?php
   
   exit; 
   
   die; 
   
   ?>
Connex PHP features
-------------------

  + `exit <https://php-dictionary.readthedocs.io/en/latest/dictionary/exit.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ExitNoArg                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


