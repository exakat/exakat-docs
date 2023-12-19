.. _structures-nodirectusage:

.. _no-direct-usage:

No Direct Usage
+++++++++++++++

  The results of the following functions shouldn't be used directly, but checked first. 

For example, `glob() <https://www.php.net/glob>`_ returns an array, unless some `error <https://www.php.net/error>`_ happens, in which case it returns a boolean (false). In such case, however rare it is, plugging `glob() <https://www.php.net/glob>`_ directly in a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loops will yield errors.


.. code-block:: php
   
   <?php
       // Used without check : 
       foreach(glob('.') as $file) { /* do Something */ }.
       
       // Used without check : 
       $files = glob('.');
       if (!is_array($files)) {
           foreach($files as $file) { /* do Something */ }.
       }
   ?>

Suggestions
___________

* Check the return of the function before using it, in particular for false, or array().




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoDirectUsage                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-edusoho-structures-nodirectusage`, :ref:`case-xoops-structures-nodirectusage`                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


