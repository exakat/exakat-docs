.. _php-hashusesobjects:

.. _hash-will-use-objects:

Hash Will Use Objects
+++++++++++++++++++++

  The `ext/hash extension <http://www.php.net/manual/en/book.hash.php>`_ used resources, and is being upgraded to use resources. 


.. code-block:: php
   
   <?php
   
   // Post 7.2 code 
       $hash = hash_init('sha256');
       if (!is_object($hash)) {
           trigger_error('error');
       }
       hash_update($hash, $message);
   
   // Pre-7.2 code
       $hash = hash_init('md5');
       if (!is_resource($hash)) {
           trigger_error('error');
       }
       hash_update($hash, $message);
   
   ?>

See also `Move ext/hash from resources to objects <https://www.php.net/manual/en/migration72.incompatible.php#migration72.incompatible.hash-ext-to-objects>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/HashUsesObjects                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | hash, object                                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


