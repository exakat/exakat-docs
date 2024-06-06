.. _files-inclusionwrongcase:

.. _inclusion-wrong-case:

Inclusion Wrong Case
++++++++++++++++++++

  Inclusion should follow exactly the case of included files and path. This prevents the infamous case-sensitive filesystem bug, where files are correctly included in a case-insensitive system, and failed to be when moved to production.

.. code-block:: php
   
   <?php
   
   // There must exist a path called "path/to" and a file "library.php" with this case
   include "path/to/library.php";
   
   // Error on the case, while the file does exist
   include "path/to/LIBRARY.php";
   
   // Error on the case, on the PATH
   include "path/TO/library.php";
   
   ?>

See also `include_once <https://www.php.net/manual/en/function.include-once.php>`_.


Suggestions
___________

* Make the inclusion string identical to the file name. 
* Change the name of the file to reflect the actual inclusion. This is the best way when a naming convention has been set up for the project, and the file doesn't adhere to it. Remember to change all other inclusion.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Files/InclusionWrongCase                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | include                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


