.. _security-directinjection:

.. _direct-injection:

Direct Injection
++++++++++++++++

  The following code act directly upon PHP incoming variables like ``$_GET`` and ``$_POST``. This makes those snippets very unsafe.

.. code-block:: php
   
   <?php
   
   // Direct injection
   echo "Hello ".$_GET['user'].", welcome.";
   
   // less direct injection
   foo($_GET['user']);
   function foo($user) {
       echo "Hello ".$user.", welcome.";
   }
   
   ?>

See also `Cross-Site Scripting (XSS) <https://phpsecurity.readthedocs.io/en/latest/Cross-Site-Scripting-(XSS).html>`_.

Connex PHP features
-------------------

  + `injection <https://php-dictionary.readthedocs.io/en/latest/dictionary/injection.ini.html>`_


Suggestions
___________

* Validate input : make sure the incoming data are what you expect from them.
* Escape output : prepare outgoing data for the next system to use.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/DirectInjection                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


