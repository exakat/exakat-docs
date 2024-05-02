.. _classes-checkoncallusage:

.. _check-on-\_\_call-usage:

Check On __Call Usage
+++++++++++++++++++++

  When using the magic methods `__call() <https://www.php.net/manual/en/language.oop5.magic.php>`_ and __staticcall(), make sure the method exists before calling it. 

If the method doesn't exists, then the same method will be called again, leading to the same failure. Finally, it will crash PHP.

.. code-block:: php
   
   <?php
   
   class safeCall {
       function __class($name, $args) {
           // unsafe call, no checks
           if (method_exists($this, $name)) {
               $this->$name(...$args);
           }
       }
   }
   
   class unsafeCall {
       function __class($name, $args) {
           // unsafe call, no checks
           $this->$name(...$args);
       }
   }
   
   ?>

See also `Method overloading <https://www.php.net/manual/en/language.oop5.overloading.php#object.call>`_ and `Magical PHP: __call <https://www.garfieldtech.com/index.php/blog/magical-php-call>`_.


Suggestions
___________

* Add a call to method_exists() before using any method name
* Relay the call to another object that doesn't handle __call() or __callStatic()




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CheckOnCallUsage                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | magic-method                                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


