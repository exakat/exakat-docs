.. _structures-uselessglobal:

.. _useless-global:

Useless Global
++++++++++++++

  Global are useless in two cases. First, on super-globals, which are always globals, like `$_GET <https://www.php.net/manual/en/reserved.variables.get.php>`_; secondly, on variables that are not used.
Also, PHP has superglobals, a special team of variables that are always available, whatever the context. 
They are : $GLOBALS, $_SERVER, `$_GET <https://www.php.net/manual/en/reserved.variables.get.php>`_, `$_POST <https://www.php.net/manual/en/reserved.variables.post.php>`_, $_FILES, $_COOKIE, $_SESSION, `$_REQUEST <https://www.php.net/manual/en/reserved.variables.request.php>`_ and `$_ENV <https://www.php.net/manual/en/reserved.variables.env.php>`_.

.. code-block:: php
   
   <?php
   
   // $_POST is already a global : it is in fact a global everywhere
   global $_POST;
   
   // $unused is useless
   function foo() {
       global $used, $unused;
       
       ++$used;
   }
   
   ?>

Suggestions
___________

* Drop the global expression




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessGlobal                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | super-global, $_get, $_post, $_server, $globals, $_files, $_cookie, $_request, $_env                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zencart-structures-uselessglobal`, :ref:`case-humo-gen-structures-uselessglobal`                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


