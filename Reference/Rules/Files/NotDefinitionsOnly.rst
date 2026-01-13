.. _files-notdefinitionsonly:

.. _file-is-not-definitions-only:

File Is Not Definitions Only
++++++++++++++++++++++++++++

  An included file should only provide definitions and declarations, or executable code : not both. 

With definitions only files, their inclusion provide new features, and keep the current execution untouched, and in control of the flow.
Within this context, globals, use, and namespaces instructions are not considered a warning.

.. code-block:: php
   
   <?php
   // This whole script is a file
   
   // It contains definitions and global code
   class foo {
       static public $foo = null;
   }
   //This can be a singleton creation
   foo::$foo = new foo();
   
   trait t {}
   
   class bar {}
   
   ?>

Suggestions
___________

* Remove the executable code from the file
* Remove the definitions from the file




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Files/NotDefinitionsOnly                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


