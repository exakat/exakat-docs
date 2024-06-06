.. _structures-unpreprocessed:

.. _unpreprocessed-values:

Unpreprocessed Values
+++++++++++++++++++++

  Preprocessing values is the preparation of values before PHP executes the code. 

There is no macro language in PHP, that prepares the code before compilation, bringing some comfort and short syntax. Most of the time, one uses PHP itself to preprocess data. 

For example : 
could be written 
and avoid preprocessing the string into an array first. 

Preprocessing could be done anytime the script includes all the needed values to process the expression. 

This is a micro-optimisation, in particular when the expression is used once.

.. code-block:: php
   
   <?php
       $days_en = 'monday,tuesday,wednesday,thursday,friday,saturday,sunday';
       $days_zh = '星期－,星期二,星期三,星期四,星期五,星期六,星期日';
   
       $days = explode(',', $lang === 'en' ? $days_en : $days_zh); 
   ?>

Suggestions
___________

* Preprocess the values and hardcode them in PHP. Do not use PHP to calculate something at the last moment.
* Use already processed values, or cache to avoid calculating the value each hit.
* Create a class that export the data in the right format for every situation, including the developer's comfort.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/Unpreprocessed                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | preprocess, micro-optimisation                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `always-preprocess <https://github.com/dseguy/clearPHP/tree/master/rules/always-preprocess.md>`__                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-structures-unpreprocessed`, :ref:`case-piwigo-structures-unpreprocessed`                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


