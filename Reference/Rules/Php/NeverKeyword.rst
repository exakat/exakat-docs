.. _php-neverkeyword:

.. _never-keyword:

Never Keyword
+++++++++++++

  Never becomes a PHP keyword. It is used for typing functions which never returns anything (either dies or throw an `exception) <https://www.php.net/exception>`_.

It should be avoided in namespaces, classes, traits and interfaces. Methods, constants and functions are OK.

.. code-block:: php
   
   <?php
   
   // This is OK
   function never() { } 
   
   // This is no OK
   class never {  } 
   
   ?>

See also `never <https://www.php.net/manual/en/language.types.declarations.php#language.types.declarations.never>`_ and `PHP RFC: noreturn type <https://wiki.php.net/rfc/noreturn_type>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Cannot+use+%27never%27+as+class+name+as+it+is+reserved+.html>`_



Connex PHP features
-------------------

  + `never <https://php-dictionary.readthedocs.io/en/latest/dictionary/never.ini.html>`_


Suggestions
___________

* Rename the classes, traits and interfaces with a different name.




Specs
_____

+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/NeverKeyword                                                                                                                                                                                         |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>` |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.3.0                                                                                                                                                                                                    |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 8.1 and older                                                                                                                                                                                   |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                                                                                    |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                                                                                            |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.1 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                                                                                                               |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                                |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                  |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


