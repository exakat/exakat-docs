.. _classes-undefinedmethod:

.. _undefined-methods:

Undefined Methods
+++++++++++++++++

  The methods used in the code are undefined. 

Defined methods are found in : 
+ Local definitions
+ `__call() <https://www.php.net/manual/en/language.oop5.magic.php>`_ definition
+ PHP native definitions
+ Extension's definitions
+ Included components.

When the origin of the class is not clear, the report is omitted.

.. code-block:: php
   
   <?php
   
   class x {
       function foo() {
           $this->defined();
           $this->undefined();
       }
       
       function defined() {}
   }
   
   ?>
Connex PHP features
-------------------

  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Suggestions
___________

* Fix the name of the method in the methodcall
* Define the method in the target class




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UndefinedMethod                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.6                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


