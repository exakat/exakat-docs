.. _functions-wrongnumberofargumentsmethods:

.. _wrong-number-of-arguments-in-methods:

Wrong Number Of Arguments In Methods
++++++++++++++++++++++++++++++++++++

  Those methods are called with a wrong number of arguments : too many or too few. Check the signature.
Methods with a variable number of argument, either using ellipsis or `func_get_args() <https://www.php.net/func_get_args>`_ are ignored. 

PHP emits an `error <https://www.php.net/error>`_ at runtime, when arguments are not enough : ''. PHP doesn't emit an `error <https://www.php.net/error>`_ when too many arguments are provided.

.. code-block:: php
   
   <?php
   
   class Foo {
       private function Bar($a, $b) {
           return $a + $b;
       }
       
       public function foobar() {
           $this->Bar(1);
           
           // Good amount
           $this->Bar(1, 2);
           
           // Too Many
           $this->Bar(1, 2, 3);
       }
   }
   
   ?>

Suggestions
___________

* Adapt the call to use one of the right number of arguments : this means dropping the extra ones, or adding the missing ones
* Adapt the signature of the method, and use a default value




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/WrongNumberOfArgumentsMethods                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | composer                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


