.. _structures-onelinetwoinstructions:

.. _several-instructions-on-the-same-line:

Several Instructions On The Same Line
+++++++++++++++++++++++++++++++++++++

  Usually, instructions do not share their line : one instruction, one line. 

This is good for readability, and help at understanding the code. This is especially important when fast-reading the code to find some special situation, where such double-meaning line way have an impact.


.. code-block:: php
   
   <?php
   
   switch ($x) {
       // Is it a fallthrough or not ? 
       case 1:
           doSomething(); break;
   
       // Easily spotted break.
       case 1:
           doSomethingElse(); 
           break;
   
       default : 
           doDefault(); 
           break;
   }
   
   ?>

See also `Object Calisthenics, rule # 5 <http://williamdurand.fr/2013/06/03/object-calisthenics/#one-dot-per-line>`_.


Suggestions
___________

* Add new lines, so that one expression is on one line




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OneLineTwoInstructions                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-piwigo-structures-onelinetwoinstructions`, :ref:`case-tine20-structures-onelinetwoinstructions`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


