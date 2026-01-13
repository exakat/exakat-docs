.. _functions-realfunctions:

.. _real-functions:

Real Functions
++++++++++++++

  Real functions, not methods.

Function keywords, that are not in a class, trait, interface, nor a `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_.

.. code-block:: php
   
   <?php
   
   // a real Function
   function realFunction () {}
   
   // Those are not real functions
   function ($closure) { }
   
   class foo {
       function isAClassMethod() {}
   }
   
   interface fooi {
       function isAnInterfaceMethod() {}
   }
   
   trait foot {
       function isATraitMethod() {}
   }
   ?>
Connex PHP features
-------------------

  + `function <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/RealFunctions                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


