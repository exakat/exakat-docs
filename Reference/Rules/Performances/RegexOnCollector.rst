.. _performances-regexoncollector:

.. _processing-collector:

Processing Collector
++++++++++++++++++++

  When accumulating data in a variable, within a loop, it is slow to apply repeatedly a function to the variable.

The example below illustrate the problem : ``$collector`` is build with element from ``$array``. ``$collector`` actually gets larger and larger, slowing the `in_array() <https://www.php.net/in_array>`_ call each time. 

It is better to apply the `preg_replace() <https://www.php.net/preg_replace>`_ to ``$a``, a short variable, and then, add ``$a`` to the collector.


.. code-block:: php
   
   <?php
   
   // Fast way
   $collector = '';
   foreach($array as $a){
       $a = preg_replace('/__(.*?)__/', '<b>$1</b>', $a);
       $collector .= $a;
   }
   
   // Slow way
   $collector = '';
   foreach($array as $a){
       $collector .= $a;
       $collector = preg_replace('/__(.*?)__/', '<b>$1</b>', $collector);
   }
   
   ?>

Suggestions
___________

* Avoid applying the checks on the whole data, rather on the diff only.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/RegexOnCollector                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


