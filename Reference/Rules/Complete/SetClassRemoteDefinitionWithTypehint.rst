.. _complete-setclassremotedefinitionwithtypehint:

.. _set-class-remote-definition-with-typehint:

Set Class Remote Definition With Typehint
+++++++++++++++++++++++++++++++++++++++++

  Links method calls, properties `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or not, and constants to their definition, thanks to typed arguments. The link is ``DEFINITION``.

.. code-block:: php
   
   <?php
   
   class x {
       public function bar() {    }
   }
   
   function foo(x $a) {
       // This links to class x, method bar(), thanks to the typehint.
       return $a->bar();
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetClassRemoteDefinitionWithTypehint                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`NoDoc <ruleset-NoDoc>`                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


