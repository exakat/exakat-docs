.. _structures-onceusage:

.. _include\_once()-usage:

include_once() Usage
++++++++++++++++++++

  Usage of include_once() and require_once(). Those functions should be avoided for performances reasons.


.. code-block:: php
   
   <?php
   
   // Including a library. 
   include 'lib/helpers.inc';
   
   // Including a library, and avoiding double inclusion
   include_once 'lib/helpers.inc';
   
   ?>


Try using autoload for loading classes, or use include() or require() and make it possible to include several times the same file without errors.

Suggestions
___________

* Avoid using include_once() whenever possible 
* Use autoload() to load classes, and avoid loading them with include




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OnceUsage                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xoops-structures-onceusage`, :ref:`case-tikiwiki-structures-onceusage`                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


