.. _structures-nohardcodedpath:

.. _no-hardcoded-path:

No Hardcoded Path
+++++++++++++++++

  It is not recommended to use hardcoded literals when designating files. Full paths are usually tied to one file system organization. As soon as the organisation changes or must be adapted to any external constraint, the path is not valid anymore.

Either use `__FILE__ <https://www.php.net/manual/en/language.constants.predefined.php>`_ and `__DIR__ <https://www.php.net/manual/en/language.constants.predefined.php>`_ to make the path relative to the current file; use a ``DOC_ROOT`` as a configuration constant that will allow the moving of the script to another folder; finally functions like `sys_get_temp_dir() <https://www.php.net/sys_get_temp_dir>`_ produce a viable temporary folder.

Relative paths are relative to the current execution `directory <https://www.php.net/`directory <https://www.php.net/directory>`_>`_, and not the current file. This means they may differ depending on the location of the start of the application, and are sensitive to `chdir() <https://www.php.net/chdir>`_ and `chroot() <https://www.php.net/chroot>`_ usage.

.. code-block:: php
   
   <?php
   
       // This depends on the current executed script
       file_get_contents('token.txt');
   
       // Exotic protocols are ignored
       file_get_contents('jackalope://file.txt');
   
       // Some protocols are ignored : http, https, ftp, ssh2, php (with memory)
       file_get_contents('http://www.php.net/');
       file_get_contents('php://memory/');
       
       // glob() with special chars * and ? are not reported
       glob('./*/foo/bar?.txt');
       // glob() without special chars * and ? are reported
       glob('/foo/bar/');
       
   ?>

Suggestions
___________

* Add __DIR__ before the path to make it relative to the current file
* Add a configured prefix before the path to point to any file in the system
* Use sys_get_temp_dir() for temporary data
* Use ``include_path`` argument function, such as fie_get_contents(), to have the file located in configurable directories.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoHardcodedPath                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
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
| Features     | path, hardcoded                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-hardcoded-path <https://github.com/dseguy/clearPHP/tree/master/rules/no-hardcoded-path.md>`__                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tine20-structures-nohardcodedpath`, :ref:`case-thelia-structures-nohardcodedpath`                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


