.. _classes-nomagicwitharray:

.. _no-magic-method-with-array:

No Magic Method With Array
++++++++++++++++++++++++++

  Magic method ``__set()`` doesn't work for array syntax. 

When overloading properties, they can only be used for scalar values, excluding arrays. Under the hood, PHP uses ``__get()`` to reach for the name of the property, and doesn't recognize the following index as an array. It yields an `error <https://www.php.net/error>`_ : "Indirect modification of overloaded property".



It is possible to use the array syntax with a magic property : by making the ``__get`` returns an array, the syntax will actually extract the expected item in the array.

This is not reported by linting.

In this analysis, only properties that are found to be magic are reported. For example, using the b property outside the class scope is not reported, as it would yield too many false-positives.

.. code-block:: php
   
   <?php
   
   class c {
       private $a;
       private $o = array();
   
       function __get($name) {
           return $this->o[$name];
       }
       
       function foo() {
           // property b doesn't exists
           $this->b['a'] = 3;
           
           print_r($this);
       }
   
       // This method has no impact on the issue
       function __set($name, $value) {
           $this->o[$name] = $value;
       }
   }
   
   $c = new c();
   $c->foo();
   
   ?>

See also `Overload <https://www.php.net/manual/en/language.oop5.overloading.php#object.get>`_.


Suggestions
___________

* Use a distinct method to append a new value to that property
* Assign the whole array, and not just one of its elements




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NoMagicWithArray                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.4                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | magic-method                                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


