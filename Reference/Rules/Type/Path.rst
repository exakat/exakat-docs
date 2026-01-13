.. _type-path:

.. _path-lists:

Path lists
++++++++++

  List of all paths that were found in the code.

Path are identified with this regex : ``^(.*/)([^/]*)\.\w+$``. In particular, the `directory <https://www.php.net/`directory <https://www.php.net/directory>`_>`_ delimiter is ``/`` : Windows delimiter ``\`` are not detected. 
URL are ignored when the protocol is present in the literal : ``http://www.example.com`` is not mistaken with a file.

.. code-block:: php
   
   <?php
   
   // the first argument is recognized as an URL
   fopen('/tmp/my/file.txt', 'r+');
   
   // the string argument  is recognized as an URL
   $source = 'https://www.other-example.com/';
   
   ?>

See also `Dir predefined constants <https://www.php.net/manual/en/dir.constants.php>`_ and `Supported Protocols and Wrappers <https://www.php.net/manual/en/wrappers.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/Path                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.8                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


