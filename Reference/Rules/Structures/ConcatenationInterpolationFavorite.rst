.. _structures-concatenationinterpolationfavorite:

.. _concatenation-interpolation-consistence:

Concatenation Interpolation Consistence
+++++++++++++++++++++++++++++++++++++++

  Concatenations are done with the . operator or by interpolation inside a string. 

Interpolation is a clean way to write concatenation, though it gets messy with long dereferences or with constants. Concatenations are longer to write. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same. 


.. code-block:: php
   
   <?php
   
   // be consistent
   $a = "$b $c";
   $d = "$b $e";
   $e = "$b $e";
   $d = "$b $f";
   $f = "$b $z";
   $h = "$b $e";
   $y = "$b $e";
   $d = "$b $x";
   $j = "$b $c";
   $d = "$b $g";
   $d = "$b $h"; 
   
   // Be consistent, always use the same syntax
   $z = $w.' '.$e;
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ConcatenationInterpolationFavorite                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.6                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | concatenation                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


