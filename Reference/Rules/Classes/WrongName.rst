.. _classes-wrongname:

.. _illegal-name-for-method:

Illegal Name For Method
+++++++++++++++++++++++

  PHP has reserved usage of methods starting with ``__`` for magic methods. It is recommended to avoid using this prefix, to prevent confusions.


.. code-block:: php
   
   <?php
   
   class foo{
       // Constructor
       function __construct() {}
   
       // Constructor's typo
       function __constructor() {}
   
       // Illegal function name, even as private
       private function __bar() {}
   }
   
   ?>

See also `Magic Methods <https://www.php.net/manual/en/language.oop5.magic.php>`_.


Suggestions
___________

* Avoid method names starting with a double underscore : ``__``
* Use method visibilities to ensure that methods are only available to the current class or its children




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/WrongName                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | method                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-prestashop-classes-wrongname`, :ref:`case-magento-classes-wrongname`                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


