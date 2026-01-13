.. _classes-directcalltomagicmethod:

.. _no-direct-call-to-magic-method:

No Direct Call To Magic Method
++++++++++++++++++++++++++++++

  PHP features magic methods, which are methods related to operators.

Magic methods, such as `__get() <https://www.php.net/manual/en/language.oop5.magic.php>`_, related to =, or `__clone() <https://www.php.net/manual/en/language.oop5.magic.php>`_, related to ``clone``, are supposed to be used in an object environment, and not with direct call. 

It is recommended to use the magic method with its intended usage, and not to call it directly. For example, typecast to ``string`` instead of calling the `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_ method.

Accessing those methods in a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ way is also discouraged.

.. code-block:: php
   
   <?php
   // Write
     print $x->a;
   // instead of 
     print $x->__get('a'); 
   
   class Foo {
       private $b = "secret";
   
       public function __toString() {
           return strtoupper($this->b);
       }
   }
   
   $bar = new Foo();
   echo (string) $bar;
   
   ?>

See also `Magical PHP: __call <https://www.garfieldtech.com/blog/magical-php-call>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DirectCallToMagicMethod                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


