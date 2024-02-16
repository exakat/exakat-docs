.. _structures-onelevelofindentation:

.. _more-than-one-level-of-indentation:

More Than One Level Of Indentation
++++++++++++++++++++++++++++++++++

  According to PHP Object Calisthenics, one level of indentation is sufficient.

It helps to abide by the Single Responsibility rule and increase reuse.


.. code-block:: php
   
   <?php
   
   class foo {
       function multipleLevels($array) {
           $return = array();
           foreach($array as $b) {
   
               // This is a second level of indentation
               if ($this->check($b)) { continue; }
               $return[] = $b;
           }
           return $return;
       }
   
       function oneLevel($array) {
           $return = array_filter($array, array($this, 'check'));
           return $return;
       }
   
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OneLevelOfIndentation                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | indentation                                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


