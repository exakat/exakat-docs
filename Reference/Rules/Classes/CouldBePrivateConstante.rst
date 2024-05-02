.. _classes-couldbeprivateconstante:

.. _could-be-private-class-constant:

Could Be Private Class Constant
+++++++++++++++++++++++++++++++

  Class constant may use ``private`` visibility. 

Since PHP 7.1, constants may also have a public/protected/private visibility. This restrict their usage to anywhere, class and children or class. 

As a general rule, it is recommended to make constant ``private`` by default, and to relax this restriction as needed. PHP makes them public by default.
Constant shall stay ``public`` when the code has to be compatible with PHP 7.0 and older. 

They also have to be public in the case of component : some of those constants have to be used by external actors, in order to configure the component.

.. code-block:: php
   
   <?php
   
   class foo {
       // pre-7.1 style
       const PRE_71_CONSTANT = 1;
       
       // post-7.1 style
       private const PRIVATE_CONSTANT = 2;
       public const PUBLIC_CONSTANT = 3;
       
       function bar() {
           // PRIVATE CONSTANT may only be used in its class
           echo self::PRIVATE_CONSTANT;
       }
   }
   
   // Other constants may be used anywhere
   function x($a = foo::PUBLIC_CONSTANT) {
       echo $a.' '.foo:PRE_71_CONSTANT;
   }
   
   ?>

See also `Class Constants <https://www.php.net/manual/en/language.oop5.constants.php>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBePrivateConstante                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.10                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | visibility                                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phinx-classes-couldbeprivateconstante`                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


