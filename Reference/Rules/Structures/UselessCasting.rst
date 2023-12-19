.. _structures-uselesscasting:

.. _useless-type-casting:

Useless Type Casting
++++++++++++++++++++

  There is no need to cast already typed values.


.. code-block:: php
   
   <?php
   
   // trim always returns a string : cast is useless
   $a = (string) trim($b);
   
   // strpos doesn't always returns an integer : cast is useful
   $a = (boolean) strpos($b, $c);
   
   // comparison don't need casting, nor parenthesis
   $c = (bool) ($b > 2);
   
   function foo(array $a) {
       foreach((array) $a as $b) {
           // doSomething
       }
   }
   ?>


Typed values, such as properties, do not have to be cast again, as the `engine <https://www.php.net/engine>`_ always ensures their type.

Typed arguments are variables : after the initial check at method call time, they might change value and type. Those extra cast may then carry some value, although changing the type of an incoming value is not recommended.

See also `Type juggling <https://www.php.net/manual/en/language.types.type-juggling.php>`_ and :ref:`Multiple Type Variable <multiple-type-variable>`.


Suggestions
___________

* Remove the type cast




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessCasting                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.7                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | type, cast                                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-fuelcms-structures-uselesscasting`, :ref:`case-thinkphp-structures-uselesscasting`                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


