.. _classes-thisisnotanarray:

.. _$this-is-not-an-array:

$this Is Not An Array
+++++++++++++++++++++

  ``$this`` variable represents the current object and it is not an array. 

This is unless the class (or its parents) has the ``ArrayAccess`` interface, or extends ``ArrayObject`` or ``SimpleXMLElement``.

.. code-block:: php
   
   <?php
   
   // $this is an array
   class Foo extends ArrayAccess {
       function bar() {
           ++$this[3];
       }
   }
   
   // $this is not an array
   class Foo2 {
       function bar() {
           ++$this[3];
       }
   }
   
   ?>

See also `ArrayAccess <https://www.php.net/manual/en/class.arrayaccess.php>`_, `ArrayObject <https://www.php.net/manual/en/class.arrayobject.php>`_ and `The Basics <https://www.php.net/manual/en/language.oop5.basic.php>`_.


Suggestions
___________

* Extends ``ArrayObject``, or a class that extends it, to use ``$this`` as an array too.
* Implements ``ArrayAccess`` to use ``$this`` as an array too.
* Use a property in the current class to store the data, instead of $this directly.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ThisIsNotAnArray                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | $this                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


