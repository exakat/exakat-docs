.. _complete-createmagicmethod:

.. _create-magic-method:

Create Magic Method
+++++++++++++++++++

  This command creates a link DEFINITION between a ``__call()`` and ``__callStatic()`` calls, and its equivalent magic method.


.. code-block:: php
   
   <?php
   
   class x {
       function foo() {
           // This is linked to __call
           $this->c();
           
           // This is linked to __callStatic
           return $this::C();
       }
       
       function __call($name, $args) {
           // Normal method call
       }
   
       function __callStatic($name, $args) {
           // Static method call
       }
   }
   
   ?>


This command may not detect all possible link for the ``__get()`` and ``__set()`` call. It may be missing information about the nature of the object. ``Self``, ``static``, ``parent`` and simple variables are detected.

See also `Magic Methods <https://www.php.net/manual/en/language.oop5.magic.php>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/CreateMagicMethod                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`NoDoc <ruleset-NoDoc>`                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | magic-method                                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


