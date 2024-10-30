.. _security-indirectinjection:

.. _indirect-injection:

Indirect Injection
++++++++++++++++++

  This rule reports injections through indirect usage of `$_GET <https://www.php.net/manual/en/reserved.variables.get.php>`_, `$_POST <https://www.php.net/manual/en/reserved.variables.post.php>`_, `$_REQUEST <https://www.php.net/manual/en/reserved.variables.request.php>`_, $_COOKIE values. The injection is indirect, as the incoming data may be stored in different container before reaching the sensitive call. 

Sensitive parameters are identified with Security/`SensitiveParameter <https://www.php.net/sensitiveparameter>`_ rule.

.. code-block:: php
   
   <?php
   
   $a = $_GET['a'];
   echo $a;
   
   function foo($b) {
       echo $b;
   }
   foo($_POST['c']);  // $_POST is propagated to the foo function
   
   ?>
Connex PHP features
-------------------

  + `injection <https://php-dictionary.readthedocs.io/en/latest/dictionary/injection.ini.html>`_


Suggestions
___________

* Always validate incoming values before using them.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/IndirectInjection                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


