.. _classes-cyclicreferences:

.. _cyclic-references:

Cyclic References
+++++++++++++++++

  Avoid cyclic references. 

Cyclic references happen when an object points to another object, which reciprocate. This is particularly possible with classes, when the child class has to keep a reference to the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class. 


.. code-block:: php
   
   <?php
   
   class a {
       private $p = null;
       
       function foo() {
           $this->p = new b();
           // the current class is stored in the child class
           $this->p->m($this);
       }
   }
   
   class b {
       private $pb = null;
       
       function n($a) {
           // the current class keeps a link to its parent
           $this->pb = $a;
       }
   }
   ?>


Cyclic references, or circular references, are memory intensive : only the garbage collector can understand when they may be flushed from memory, which is a costly operation. On the other hand, in an acyclic reference code, the reference counter will know immediately know that an object is free or not.

See also `About circular references in PHP <https://johann.pardanaud.com/blog/about-circular-references-in-php>`_ and `A Journey to find a memory leak <https://jolicode.com/blog/a-journey-to-find-a-memory-leak/>`_.


Suggestions
___________

* Use a different object when calling the child objects. 
* Refactor your code to avoid the cyclic reference.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CyclicReferences                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | class, extends                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


