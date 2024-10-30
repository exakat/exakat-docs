.. _structures-couldusearraysum:

.. _could-use-array\_sum():

Could Use array_sum()
+++++++++++++++++++++

  These loops could use `array_sum() <https://www.php.net/array_sum>`_. `array_sum() <https://www.php.net/array_sum>`_ loops over the array and sum all of its elements. It is a native PHP function, faster to execute and easier to read.
When the added elements are, in fact, arrays, use `array_merge() <https://www.php.net/array_merge>`_ instead of `array_sum() <https://www.php.net/array_sum>`_.

This is a micro-optimisation : it will speed up the code, but won't bring large improvements.

.. code-block:: php
   
   <?php
   
   $total = 0;
   foreach($array as $b) {
       $total = $total + $b;
   }
   
   ?>
Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Replace the loop with a call to array_sum().




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldUseArraySum                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


