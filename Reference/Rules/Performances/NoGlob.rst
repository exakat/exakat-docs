.. _performances-noglob:

.. _avoid-glob()-usage:

Avoid glob() Usage
++++++++++++++++++

  `glob() <https://www.php.net/glob>`_ and `scandir() <https://www.php.net/scandir>`_ sorts results by default. When that kind of sorting is not needed, save some time by requesting ``NOSORT`` with those functions.

Besides, whenever possible, use `scandir() <https://www.php.net/scandir>`_ instead of `glob() <https://www.php.net/glob>`_. 
Using `opendir() <https://www.php.net/opendir>`_ and a while loop may be even faster. 

This analysis skips `scandir() <https://www.php.net/scandir>`_ and `glob() <https://www.php.net/glob>`_ if they are explicitly configured with flags (aka, sorting is explicitly needed).

`glob() <https://www.php.net/glob>`_ accepts wildchar, such as ``*``, that may not easily replaced with `scandir() <https://www.php.net/scandir>`_ or `opendir() <https://www.php.net/opendir>`_.

.. code-block:: php
   
   <?php
   
   // Scandir without sorting is the fastest. 
   scandir('docs/', SCANDIR_SORT_NONE);
   
   // Scandir sorts files by default. Same as above, but with sorting
   scandir('docs/');
   
   // glob sorts files by default. Same as below, but no sorting
   glob('docs/*', GLOB_NOSORT);
   
   // glob sorts files by default. This is the slowest version
   glob('docs/*');
   
   ?>

See also `Putting glob to the test <https://www.phparch.com/2010/04/putting-glob-to-the-test/>`_, `How to list files recursively in a directory with PHP iterators  <https://dev.to/bdelespierre/how-to-list-files-recursively-in-a-directory-with-php-iterators-5c0m>`_ and `glob:// <https://www.php.net/manual/en/wrappers.glob.php>`_.


Suggestions
___________

* Use ``FilesystemIterator`` or ``DirectoryIterator`` classes.
* Use ``RegexIterator`` to filter any unwanted results from ``FilesystemIterator``.
* Use ``glob`` protocol for files : $it = new DirectoryIterator('glob://path/to/examples/*.php');




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/NoGlob                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.6                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Features     | glob, directoryiterator, filesystemiterator                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phinx-performances-noglob`, :ref:`case-nextcloud-performances-noglob`                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


