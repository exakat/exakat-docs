.. _type-stringinterpolation:

.. _interpolation:

Interpolation
+++++++++++++

  The following strings contain variables that are will be replaced. However, the following characters are ambiguous, and may lead to confusion. 



It is advised to add curly brackets around those structures to make them non-ambiguous.

.. code-block:: php
   
   <?php
   
   class b { 
       public $b = 'c';
       function __toString() { return __CLASS__; }
   }
   $x = array(1 => new B());
   
   // -> after the $x[1] looks like a 2nd dereferencing, but it is not. 
   print "$x[1]->b";
   // displays : b->b
   
   print "{$x[1]->b}";
   // displays : c
   
   ?>

See also `Double quoted <https://www.php.net/manual/en/language.types.string.php#language.types.string.syntax.double>`_.


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/StringInterpolation                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Features     | string, interpolation                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


