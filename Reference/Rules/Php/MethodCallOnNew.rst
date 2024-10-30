.. _php-methodcallonnew:

.. _methodcall-on-new:

Methodcall On New
+++++++++++++++++

  It is possible to call a method right at object instantiation. 

This syntax was added in PHP 5.4+. Before, this was not possible : the object had to be stored in a variable first.
This syntax is interesting when the object is not reused, and may be discarded

.. code-block:: php
   
   <?php
   
   // Data is collected
   $data = data_source();
   
   // Data is saved, but won't be reused from this databaseRow object. It may be ignored.
   $result = (new databaseRow($data))->save();
   
   // The actual result of the save() is collected and tested.
   if ($result !== true) {
       processSaveError($data);
   }
   
   ?>
Connex PHP features
-------------------

  + `new <https://php-dictionary.readthedocs.io/en/latest/dictionary/new.ini.html>`_
  + `methodcall <https://php-dictionary.readthedocs.io/en/latest/dictionary/methodcall.ini.html>`_


Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/MethodCallOnNew                                                                                                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 5.4 and more recent                                                                                                         |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 5.4 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                                           |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


