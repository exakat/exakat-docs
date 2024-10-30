.. _php-foreachobject:

.. _foreach-on-object:

Foreach On Object
+++++++++++++++++

  Foreach on object looks like a typo. This is particularly true when both object and member are variables.

Foreach on an object member is a legit PHP syntax, though it is very rare : blind variables rarely have to be securing in an object to be processed.

.. code-block:: php
   
   <?php
   
   // This is the real thing
   foreach($array as $o => $b) { 
       doSomething();
   }
   
   // Looks suspicious
   foreach($array as $o -> $b) { 
       doSomething();
   }
   
   ?>
Connex PHP features
-------------------

  + `foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_
  + `loop <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ForeachObject                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


