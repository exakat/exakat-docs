.. _structures-shoulduseforeach:

.. _should-use-foreach:

Should Use Foreach
++++++++++++++++++

  Use the ``foreach`` loop instead of ``for`` when traversing an array.

`Foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ is the modern loop : it maps automatically every element of the array to a blind variable, and iterate. This is faster and safer.

.. code-block:: php
   
   <?php
   
   // Foreach version
   foreach($array as $element) {
       doSomething($element);
   }
   
   // The above case may even be upgraded with array_map and a callback, 
   // for the simplest one of them
   $array = array_map('doSomething', $array);
   
   // For version (one of various alternatives)
   for($i = 0; $i < count($array); $i++) {
       $element = $array[$i];
       doSomething($element);
   }
   
   // Based on array_pop or array_shift()
   while($value = array_pop($array)) {
       doSomething($array);
   }
   
   ?>

See also `foreach <https://www.php.net/manual/en/control-structures.foreach.php>`_ and `5 Ways To Loop Through An Array In PHP <https://www.codewall.co.uk/5-ways-to-loop-through-array-php/>`_.


Suggestions
___________

* Move for() loops to foreach(), whenever they apply to a finite list of elements




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ShouldUseForeach                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.7                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | foreach, for                                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-expressionengine-structures-shoulduseforeach`, :ref:`case-woocommerce-structures-shoulduseforeach`           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


