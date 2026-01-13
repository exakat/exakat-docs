.. _php-listwithappends:

.. _list-with-array-appends:

List With Array Appends
+++++++++++++++++++++++

  `List() <https://www.php.net/list>`_ behavior has changed in PHP 7.0 and it has impact on the indexing when list is used with the [] operator. 

The appended values are created in the same order than in the syntax, while in PHP 5.6, it is in the reverse order. 
In PHP 7.0, results are :::

   
   Array
   (
       [0] => 1
       [1] => 2
       [2] => 3
   )
   


In PHP 5.6, results are :::

   
   Array
   (
       [0] => 3
       [1] => 2
       [2] => 1
   )
   


.. code-block:: php
   
   <?php
   
   $x = array();
   list($x[], $x[], $x[]) = [1, 2, 3];
   
   print_r($x);
   
   ?>
Connex PHP features
-------------------

  + `list <https://php-dictionary.readthedocs.io/en/latest/dictionary/list.ini.html>`_
  + `append <https://php-dictionary.readthedocs.io/en/latest/dictionary/append.ini.html>`_


Suggestions
___________

* Refactor code to avoid using append in a list() call




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/ListWithAppends                                                                                                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                                           |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


