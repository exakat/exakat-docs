.. _classes-constructor:

.. _constructors:

Constructors
++++++++++++

  This rule marks methods as constructors. In PHP 8.0 and more recent, only the magic method ``__construct`` is the constructor. In older versions, the method with the same name than the class was the constructor, although with a lower priority than the magic method.

.. code-block:: php
   
   <?php
   
   class x {
       // Normal constructor
       function __construct() {}
   }
   
   class y {
       // Old style constructor, obsolete since PHP 7.1
       function y() {}
   }
   
   class z {
       // Normal constructor
       function __construct() {}
   
       // Old style constructor, but with lower priority
       function z() {}
   }
   
   ?>

See also `Constructors and Destructors <https://www.php.net/manual/en/language.oop5.decon.php>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/Constructor                                                                                                     |
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
| Features     | class, constructor                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


