.. _functions-cancelledparameter:

.. _cancelled-parameter:

Cancelled Parameter
+++++++++++++++++++

  A parameter is cancelled, when its value is hardcoded, and cannot be changed by the calling expression. The argument is in the signature, but it is later hardcoded to a literal value : thus, it is not usable, from the caller point of view.

Reference argument are omitted in this rule, as their value changes, however hardcoded, may have an impact on the calling code.

.. code-block:: php
   
   <?php
   
   function foo($a, $b) {
       // $b is cancelled, and cannot be changed.
       $b = 3;
   
       // $a is the only parameter here
       return $a + $b;
   }
   
   function bar($a, $b) {
       // $b is actually processed
       $c = $b;
       $c = process($c);
       
       $b = $c;
   
       // $a is the only parameter here
       return $a + $b;
   }
   
   ?>
Connex PHP features
-------------------

  + `parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/parameter.ini.html>`_


Suggestions
___________

* Remove the parameter in the method signature




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/CancelledParameter                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                   |
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


