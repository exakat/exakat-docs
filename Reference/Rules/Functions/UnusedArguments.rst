.. _functions-unusedarguments:

.. _unused-parameter:

Unused Parameter
++++++++++++++++

  Those parameters are not used in the method or function. 

Unused parameters should be removed in functions : they are dead code.

Unused parameters also should be removed from methods, though there may have external reasons for them to stay. In particular, they might be defined in a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class, or an interface, and cannot be removed.


.. code-block:: php
   
   <?php
   
   // $unused is in the signature, but not used. 
   function foo($unused, $b, $c) {
       return $b + $c;
   }
   
   interface i {
       function goo($a);
   }
   
   class a implements i {
       // goo signature comes from the interface
       function goo($a) {
           return 3;
       }
   }
   ?>

Suggestions
___________

* Drop the argument from the signature
* Actually use that argument in the body of the method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UnusedArguments                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
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
| Features     | parameter                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-thinkphp-functions-unusedarguments`, :ref:`case-phpmyadmin-functions-unusedarguments`                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


