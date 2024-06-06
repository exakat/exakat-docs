.. _classes-classoverreach:

.. _class-overreach:

Class Overreach
+++++++++++++++

  An object of class A may reach any private or protected properties, constants or methods in another object of the same class. This is a PHP feature, though seldom known.

This feature is also called class invasion.

.. code-block:: php
   
   <?php
   
   class A {
       private $p = 1;
       
       public function foo(A $a) {
           return $a->p + 1;
       }
   }
   
   echo (new A)->foo(new A);
   
   ?>

See also `Visibility from other objects <https://www.php.net/manual/en/language.oop5.visibility.php#language.oop5.visibility-other-objects>`_ and `spatie/invade <https://github.com/spatie/invade>`_.


Suggestions
___________

* Use a getter to reach inside the other object private properties




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ClassOverreach                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | visibility, class-invasion                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


