.. _classes-usethis:

.. _use-this:

Use This
++++++++

  Those methods should be using `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_, or a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method or property.

A method that doesn't use any local data may be considered for a move : may be it doesn't belong here. 

The following functioncalls have been added, as access to the current class, without using `$this` or `self` : 

+ `get_class() <https://www.php.net/get_class>`_
+ `get_called_class() <https://www.php.net/get_called_class>`_
+ `get_object_vars() <https://www.php.net/get_object_vars>`_
+ `get_parent_class() <https://www.php.net/get_parent_class>`_
+ `get_class_vars() <https://www.php.net/get_class_vars>`_
+ `get_class_methods() <https://www.php.net/get_class_methods>`_


.. code-block:: php
   
   <?php
   
   class dog {
       private $name = 'Rex';
       
       // This method is related to the current object and class
       public function attaboy() {
           return Fetch, $this->name, Fetch\n;
       }
   
       // Not using any class related data : Does this belong here?
       public function addition($a, $b) {
           return $a + $b;
       }
   }
   ?>

See also `The Basics <https://www.php.net/manual/en/language.oop5.basic.php>`_.


Suggestions
___________

* Add any use of $this pseudo-variable
* Move the method to another class
* Refactor the method as a function




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UseThis                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | this, self, static                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


