.. _complete-setclassmethodremotedefinition:

.. _set-class-method-remote-definition:

Set Class Method Remote Definition
++++++++++++++++++++++++++++++++++

  Links method to the method definition. The link is ``DEFINITION``.

`Static <https://www.php.net/manual/en/language.oop5.static.php>`_ method calls and normal method calls are both solved with this rule. `Parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ classes and trait are also searched for the right method.

.. code-block:: php
   
   <?php
   
   class x {
       public function __construct() {}
       public function foo() {}
   }
   
   // This links to __construct method
   $a = new x;
   
   // This links to foo() method
   $a->foo();
   
   ?>
Connex PHP features
-------------------

  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetClassMethodRemoteDefinition                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                   |
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


