.. _classes-undefinedparentmp:

.. _undefined-parent:

Undefined Parent
++++++++++++++++

  List of properties and methods that are accessed using ``parent`` keyword but are not defined in the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ classes. 

This may compile but, eventually yields a fatal `error <https://www.php.net/error>`_ during execution.



Note that if the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ is defined using ``extends someClass`` but ``someClass`` is not available in the tested code, it will not be reported : it may be in composer, another dependency, or just missing.

.. code-block:: php
   
   <?php
   
   class theParent {
       // No bar() method
       // private bar() method is not accessible to theChild 
   }
   
   class theChild extends theParent {
       function foo() {
           // bar is defined in theChild, but not theParent
           parent::bar();
       }
       
       function bar() {
       
       }
   }
   
   ?>

See also `parent <https://www.php.net/manual/en/keyword.parent.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Call+to+undefined+method+theParent%3A%3Abar%28%29.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/Cannot+access+parent%3A%3A+when+current+class+scope+has+no+parent.html>`_



Connex PHP features
-------------------

  + `parent <https://php-dictionary.readthedocs.io/en/latest/dictionary/parent.ini.html>`_


Suggestions
___________

* Remove the usage of the found method
* Add a definition for the method in the appropriate parent
* Fix the name of the method, and replace it with a valid definition
* Change 'parent' with 'self' if the method is eventually defined in the current class
* Change 'parent' with another object, if the method has been defined in another class
* Add the 'extends' keyword to the class, to actually have a parent class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UndefinedParentMP                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


