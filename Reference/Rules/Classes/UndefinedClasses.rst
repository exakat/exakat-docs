.. _classes-undefinedclasses:

.. _undefined-classes:

Undefined Classes
+++++++++++++++++

  Those classes are used in the code, but there are no definition for them.

This may happens under normal conditions, if the application makes use of an unsupported extension, that defines extra classes; 
or if some external libraries, such as PEAR, are not provided during the analysis.



This analysis also checks in attributes.

.. code-block:: php
   
   <?php
   
   // FPDF is a classic PDF class, that is usually omitted by Exakat. 
   $o = new FPDF();
   
   // Exakat reports undefined classes in instanceof
   // PHP ignores them
   if ($o instanceof SomeClass) {
       // doSomething();
   }
   
   // Classes may be used in typehint too
   function foo(TypeHintClass $x) {
       // doSomething();
   }
   
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Fix the typo in the class name
* Add a missing 'use' expression
* Create the missing class
* Added a missing component




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UndefinedClasses                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


