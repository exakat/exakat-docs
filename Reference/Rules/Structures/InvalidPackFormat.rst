.. _structures-invalidpackformat:

.. _invalid-pack-format:

Invalid Pack Format
+++++++++++++++++++

  Some characters are invalid in a `pack() <https://www.php.net/pack>`_ format string.

`pack() <https://www.php.net/pack>`_ and `unpack() <https://www.php.net/unpack>`_ accept the following format specifiers : ``aAhHcCsSnviIlLNVqQJPfgGdeExXZ``. 

`unpack() <https://www.php.net/unpack>`_ also accepts a name after the format specifier and an optional quantifier. 

All other situations is not a valid, and produces a warning : ``pack(): Type t: unknown format code``
Check `pack() <https://www.php.net/pack>`_ documentation for format specifiers that were introduced in various PHP version, namely 7.0, 7.1 and 7.2.

.. code-block:: php
   
   <?php
       $binarydata = pack("nvc*", 0x1234, 0x5678, 65, 66);
       
       // the first unsigned short is stored as 'first'. The next matches are names with numbers.
       $res = unpack('nfirst/vc*', $binarydata);
   ?>

See also `pack <https://www.php.net/pack>`_ and `unpack <https://www.php.net/pack>`_.


Suggestions
___________

* Fix the packing format with correct values




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/InvalidPackFormat                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.9                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | pack                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


