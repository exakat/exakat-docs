.. _structures-noobjectasindex:

.. _no-object-as-index:

No Object As Index
++++++++++++++++++

  PHP accepts objects as index, though it will report various `error <https://www.php.net/error>`_ messages when this happens.
Thanks to `George Peter Banyard <https://twitter.com/Girgias>`_ for the inspiration.

.. code-block:: php
   
   <?php
   
   $s = 'Hello';
   $o = new stdClass();
   
   try {
       $s[$o] = 'A';
   } catch (\Throwable $e) {
       echo $e->getMessage(), "\n";
       //Cannot access offset of type stdClass on string
   }
   
   ?>

See also `Use an object as an offet <https://twitter.com/Girgias/status/1405519800575553540>`_.


Suggestions
___________

* Filter values being used as index
* Filter values being used as array




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoObjectAsIndex                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | index                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


