.. _structures-shouldpreprocess:

.. _preprocessable:

Preprocessable
++++++++++++++

  The following expressions are made of literals or already known values : they may be fully calculated before running PHP.
By doing so, this will reduce the amount of work of PHP. This is a micro-optimisation, when this is used once, or the amount of work is small. It may be kept for readability.

.. code-block:: php
   
   <?php
   
   // Building an array from a string
   $name = 'PHP'.' '.'7.2';
   
   // Building an array from a string
   $list = explode(',', 'a,b,c,d,e,f');
   
   // Calculating a power
   $kbytes = $bytes / pow(2, 10);
   
   // This will never change
   $name = ucfirst(strtolower('PARIS'));
   
   ?>

Suggestions
___________

* Do the work yourself, instead of giving it to PHP




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ShouldPreprocess                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Rector <ruleset-Rector>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | preprocess, readability                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpadsnew-structures-shouldpreprocess`                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------+


