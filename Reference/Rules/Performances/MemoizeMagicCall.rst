.. _performances-memoizemagiccall:

.. _memoize-magiccall:

Memoize MagicCall
+++++++++++++++++

  Cache calls to magic methods in local variable. Local cache is faster than calling again the magic method as soon as the second call, provided that the value hasn't changed.

``__get`` is slower, as it turns a simple member access into a full method call. 
The caching is not possible if the processing of the object changes the value of the property.

.. code-block:: php
   
   <?php
   
   class x {
       private $values = array();
       
       function __get($name) {
           return $this->values[$name];
       }
       // more code to set values to this class
   }
   
   function foo(x $b) {
       $a = $b->a; 
       $c = $b->c;
       
       $d = $c;     // using local cache, no new access to $b->__get($name)
       $e = $b->a;  // Second access to $b->a, through __get
   }
   
   function bar(x $b) {
       $a = $b->a; 
       $c = $b->c;
       
       $b->bar2(); // this changes $b->a and $b->c, but we don't see it
       
       $d = $b->c; 
       $e = $b->a;  // Second access to $b->a, through __get
   }
   
   ?>

+--------------------+---------+---------+-------------------------------------------------------------------------------+
| Name               | Default | Type    | Description                                                                   |
+--------------------+---------+---------+-------------------------------------------------------------------------------+
| minMagicCallsToGet | 2       | integer | Minimal number of calls of a magic property to make it worth locally caching. |
+--------------------+---------+---------+-------------------------------------------------------------------------------+



See also `__get performance questions with PHP <https://stackoverflow.com/questions/3330852/get-set-call-performance-questions-with-php>`_, :ref:`Make Magic Concrete <make-magic-concrete>` and `Benchmarking magic <https://www.garfieldtech.com/blog/benchmarking-magic>`_.

Connex PHP features
-------------------

  + `memoization <https://php-dictionary.readthedocs.io/en/latest/dictionary/memoization.ini.html>`_


Suggestions
___________

* Cache the value in a local variable, and reuse that variable
* Make the property concrete in the class, so as to avoid __get() altogether




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/MemoizeMagicCall                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.3                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


