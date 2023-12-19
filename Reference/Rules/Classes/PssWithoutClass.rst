.. _classes-psswithoutclass:

.. _parent,-static-or-self-outside-class:

Parent, Static Or Self Outside Class
++++++++++++++++++++++++++++++++++++

  `Parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ and `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ keywords must be used within a class, a trait or an enum. They make no sense outside a class or trait scope, as `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ refers to the current class and `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ refers to one of `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ above.

PHP 7.0 and later detect some of their usage at compile time, and emits a fatal `error <https://www.php.net/error>`_.


.. code-block:: php
   
   <?php
   
   class x {
       const Y = 1;
       
       function foo() {
           // self is \x
           echo self::Y;
       }
   }
   
   const Z = 1;
   // This lint but won't anymore
   echo self::Z;
   
   ?>


`Static <https://www.php.net/manual/en/language.oop5.static.php>`_ may be used in a function or a `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, but not globally.

Suggestions
___________

* Make sure the keyword is inside a class context




Specs
_____

+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name       | Classes/PssWithoutClass                                                                                                 |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                     |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                         |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0                                                                                                                 |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                               |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Features         | parent, self, static, class                                                                                             |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-------------------------------------------------------------------------------------------------------------------------+


