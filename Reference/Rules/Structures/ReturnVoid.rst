.. _structures-returnvoid:

.. _return-void-:

Return void 
++++++++++++

  Return returns null as default value. It is recommended to mention explicitly 'null' or find a meaningful return such as a boolean or a default value instead.

.. code-block:: php
   
   <?php
   
   function foo(&$a) {
       ++$a;
       // No explicit return : it returns void
   }
   
   function bar(&$a) {
       ++$a;
       
       // Explicit return : it returns null
       return null
   }
   
   ?>

See also `Void functions <https://www.php.net/manual/en/migration71.new-features.php#migration71.new-features.void-functions>`_.

Connex PHP features
-------------------

  + `void <https://php-dictionary.readthedocs.io/en/latest/dictionary/void.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ReturnVoid                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


