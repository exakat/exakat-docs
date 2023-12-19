.. _classes-parentfirst:

.. _parent-first:

Parent First
++++++++++++

  When calling `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ constructor, always put it first in the ``__construct`` method. 

It ensures the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ is correctly build before the child start using values. 


.. code-block:: php
   
   <?php
   
   class father {
       protected $name = null;
       
       function __construct() {
           $this->name = init();
       }
   }
   
   class goodSon {
       function __construct() {
           // parent is build immediately, 
           parent::__construct();
           echo "my name is ".$this->name;
       }
   }
   
   class badSon {
       function __construct() {
           // This will fail.
           echo "my name is ".$this->name;
   
           // parent is build later, 
           parent::__construct();
       }
   }
   
   ?>


This analysis doesn't apply to Exceptions.

Suggestions
___________

* Use ``parent::__construct`` as the first call in the constructor.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ParentFirst                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Suggestions <ruleset-Suggestions>`                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | parent                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-shopware-classes-parentfirst`, :ref:`case-prestashop-classes-parentfirst`                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


