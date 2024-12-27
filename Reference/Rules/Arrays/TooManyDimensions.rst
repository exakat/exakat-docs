.. _arrays-toomanydimensions:

.. _too-many-array-dimensions:

Too Many Array Dimensions
+++++++++++++++++++++++++

  This analysis reports when arrays have too many dimensions. This happens when arrays are too deeply nested inside other arrays. 

PHP has no nesting limit, and accepts any number of of dimensions. This is usually very memory hungry, and could be better replaced with classes.

The default threshold for this rule is 3 (see examples above).

.. code-block:: php
   
   <?php
   
   $a          = array();   // level 1;
   $a[1]       = array();   // level 2
   $a[1][2]    = array();   // level 3 : still valid by default
   $a[1][2][3] = array();   // level 4 
   
   ?>

+---------------+---------+---------+-----------------------------------------+
| Name          | Default | Type    | Description                             |
+---------------+---------+---------+-----------------------------------------+
| maxDimensions | 3       | integer | Number of valid dimensions in an array. |
+---------------+---------+---------+-----------------------------------------+


Connex PHP features
-------------------

  + `multidimensional-array <https://php-dictionary.readthedocs.io/en/latest/dictionary/multidimensional-array.ini.html>`_


Suggestions
___________

* Replace the arrays by classes
* Flatten the structure of the arrays




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/TooManyDimensions                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.4                                                                                                                   |
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


