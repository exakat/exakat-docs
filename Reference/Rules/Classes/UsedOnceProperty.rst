.. _classes-usedonceproperty:

.. _used-once-property:

Used Once Property
++++++++++++++++++

  Property used once in their defining class. 

Properties used in one method only may be used several times, and read only. This may be a class constant. Such properties are meant to be overwritten by an extending class, and that's possible with class constants. 

Setting properties with default values is a good way to avoid littering the code with literal values, and provide a single point of update (by extension, or by hardcoding) for all those situations. A constant is definitely better suited for this task.

.. code-block:: php
   
   <?php
   
   class foo {
       private $defaultCols = '*';
       cont DEFAULT_COLUMNS = '*';
   
       // $this->defaultCols holds a default value. Should be a constant.
       function bar($table, $cols) {
           // This is necessary to activate usage of default values
           if (empty($cols)) {
               $cols = $this->defaultCols;
           }
           $res = $this->query('SELECT '.$cols.' FROM '.$table);
           // ....
       }
   
       // Upgraded version of bar, with default values
       function bar2($table, $cols = self::DEFAULT_COLUMNS) {
           $res = $this->query('SELECT '.$cols.' FROM '.$table);
           // .....
       }
   }
   
   ?>

Suggestions
___________

* Remove the property, as it is probably not unused
* Add another usage of the property where it is useful




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UsedOnceProperty                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.3                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | method                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


