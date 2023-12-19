.. _structures-uncheckedresources:

.. _unchecked-resources:

Unchecked Resources
+++++++++++++++++++

  Resources are created, but never checked before being used. This is not safe.

Always check that resources are correctly created before using them.


.. code-block:: php
   
   <?php
   
   // always check that the resource is created correctly
   $fp = fopen($d,'r');
   if ($fp === false) {
       throw new Exception('File not found');
   } 
   $firstLine = fread($fp);
   
   // This directory is not checked : the path may not exist and return false
   $uncheckedDir = opendir($pathToDir);
   while(readdir($uncheckedDir)) {
       // do something()
   }
   
   // This file is not checked : the path may not exist or be unreadable and return false
   $fp = fopen($pathToFile);
   while($line = freads($fp)) {
       $text .= $line;
   }
   
   // unsafe one-liner : using bzclose on an unchecked resource
   bzclose(bzopen('file'));
   
   ?>

See also `resources <https://www.php.net/manual/en/language.types.resource.php>`_.


Suggestions
___________

* Add a check between the resource acquisition and its usage




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UncheckedResources                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | resource                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-unchecked-resources <https://github.com/dseguy/clearPHP/tree/master/rules/no-unchecked-resources.md>`__                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


