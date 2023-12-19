.. _classes-makemagicconcrete:

.. _make-magic-concrete:

Make Magic Concrete
+++++++++++++++++++

  Speed up execution by replacing magic calls by concrete properties. 

Magic properties are managed dynamically, with `__get() <https://www.php.net/manual/en/language.oop5.magic.php>`_ and `__set() <https://www.php.net/manual/en/language.oop5.magic.php>`_. They replace property access by a methodcall, and they are much slower than the first. 

When a property name is getting used more often, it is worth creating a concrete property, and skip the method call. The threshold for ``magicMemberUsage`` is 1, by default. 


.. code-block:: php
   
   <?php
   
   class x {
       private $values = array('a' => 1,
                               'b' => 2);
                               
       function __get($name) {
           return $this->values[$name] ?? '';
       }
   }
   
   $x = new x();
   // Access to 'a' is repeated in the code, at least 'magicMemberUsage' time (cf configuration below)
   echo $x->a; 
   
   ?>

+------------------+---------+---------+---------------------------------------------------------------------------------------+
| Name             | Default | Type    | Description                                                                           |
+------------------+---------+---------+---------------------------------------------------------------------------------------+
| magicMemberUsage | 1       | integer | Minimal number of magic member usage across the code, to trigger a concrete property. |
+------------------+---------+---------+---------------------------------------------------------------------------------------+



See also :ref:`Memoize MagicCall <memoize-magiccall>`.


Suggestions
___________

* Make frequently used properties concrete; keep the highly dynamic as magic




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MakeMagicConcrete                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | magic-method                                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


