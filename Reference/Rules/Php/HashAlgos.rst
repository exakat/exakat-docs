.. _php-hashalgos:

.. _hash-algorithms:

Hash Algorithms
+++++++++++++++

  There is a long but limited list of hashing algorithm available to PHP. The one found doesn't seem to be existing.

.. code-block:: php
   
   <?php
   
   // This hash has existed in PHP. Check with hash_algos() if it is available on your system. 
   echo hash('ripmed160', 'The quick brown fox jumped over the lazy dog.');
   
   // This hash doesn't exist
   echo hash('ripemd160', 'The quick brown fox jumped over the lazy dog.');
   
   ?>

See also `hash_algos <https://www.php.net/hash_algos>`_.

Connex PHP features
-------------------

  + `hash <https://php-dictionary.readthedocs.io/en/latest/dictionary/hash.ini.html>`_


Suggestions
___________

* Use a hash algorithm that is available on several PHP versions
* Fix the name of the hash algorithm




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/HashAlgos                                                                                                           |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


