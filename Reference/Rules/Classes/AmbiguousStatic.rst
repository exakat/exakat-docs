.. _classes-ambiguousstatic:

.. _ambiguous-static:

Ambiguous Static
++++++++++++++++

  Methods or properties with the same name, are defined `static <https://www.php.net/manual/en/language.oop5.static.php>`_ in one class, and not `static <https://www.php.net/manual/en/language.oop5.static.php>`_ in another. This is `error <https://www.php.net/error>`_ prone, as it requires a good knowledge of the code to make it `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or not. 

Try to keep the methods simple and unique. Consider renaming the methods and properties to distinguish them easily. A method and a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method have probably different responsibilities.

.. code-block:: php
   
   <?php
   
   class a {
       function mixedStaticMethod() {}
   }
   
   class b {
       static function mixedStaticMethod() {}
   }
   
   /... a lot more code later .../
   
   $c->mixedStaticMethod();
   // or 
   $c::mixedStaticMethod();
   
   ?>

Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/AmbiguousStatic                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.3                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | static                                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


