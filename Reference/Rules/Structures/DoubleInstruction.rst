.. _structures-doubleinstruction:

.. _double-instructions:

Double Instructions
+++++++++++++++++++

  Twice the same call in a row. This might be a typo, and the second call is useless. 

It may also be an non-idempotent method: that is, a method which has a different `result <https://www.php.net/result>`_ when called with the same arguments. For example, ``rand()`` or ``fgets()``.

.. code-block:: php
   
   <?php
   
   // repetition of the same command, with the same effect each time. 
   $a = array_merge($b, $c);
   $a = array_merge($b, $c);
   
   // false positive : commands are identical, but the effect is compounded 
   $a = array_merge($a, $c);
   $a = array_merge($a, $c);
   
   ?>
Connex PHP features
-------------------

  + `idempotent <https://php-dictionary.readthedocs.io/en/latest/dictionary/idempotent.ini.html>`_


Suggestions
___________

* Remove double work
* Avoid repetition by using loops, variadic or quantifiers `(dirname($path, 2))`




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DoubleInstruction                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


