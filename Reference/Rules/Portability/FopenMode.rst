.. _portability-fopenmode:

.. _fopen-binary-mode:

Fopen Binary Mode
+++++++++++++++++

  Use explicit ``b`` when opening files.

`fopen() <https://www.php.net/fopen>`_ supports a ``b`` option in the second parameter, to make sure the read is binary. This is the recommended way when writing portable applications, between Linux and Windows.
Also, Windows PHP does support a ``t`` option, that translates automatically line endings to the right value. As this is Windows only, this should be avoided for portability reasons.

.. code-block:: php
   
   <?php
   
   // This opens file with binary reads on every OS
   $fp = fopen('path/to/file.doc', 'wb');
   
   // This may not open files with binary mode on Windows
   $fp = fopen('path/to/file.doc', 'w');
   
   ?>

See also `fopen <https://www.php.net/fopen>`_.


Suggestions
___________

* Add the `b` option when opening files




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Portability/FopenMode                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | file                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


