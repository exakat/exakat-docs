.. _structures-objectreferences:

.. _objects-don't-need-references:

Objects Don't Need References
+++++++++++++++++++++++++++++

  There is no need to add references to parameters for objects, as those are always passed by reference when used as arguments.

Reference operator is needed when the object are replaced inside the method with a new value (or a clone), as whole. Calls to methods or property modifications do not require extra reference.

Reference operator is also needed when one of the types is scalar : this include null, and the hidden null type : that is when the default value is null.

This rule applies to arguments in methods, and to `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ blind variables. 


.. code-block:: php
   
   <?php
       $object = new stdClass();
       $object->name = 'a';
       
       foo($object);
       print $object->name; // Name is 'b'
       
       // No need to make $o a reference
       function foo(&$o) {
           $o->name = 'b';
       }
   
       // $o is assigned inside the function : the parameter must have a &, or the new object won't make it out of the foo3 scope
       function foo3(&$o) {
           $o = new stdClass;
       }
   
       $array = array($object);
       foreach($array as &$o) { // No need to make this a reference
           $o->name = 'c';
       }
   
   ?>

See also `Passing by reference <https://www.php.net/manual/en/language.references.pass.php>`_.


Suggestions
___________

* Remove the reference
* Assign the argument with a new value




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ObjectReferences                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Top10 <ruleset-Top10>`                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | reference                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-references-on-objects <https://github.com/dseguy/clearPHP/tree/master/rules/no-references-on-objects.md>`__                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zencart-structures-objectreferences`, :ref:`case-xoops-structures-objectreferences`                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


