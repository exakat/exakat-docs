.. _php-dontpolluteglobalspace:

.. _don't-pollute-global-space:

Don't Pollute Global Space
++++++++++++++++++++++++++

  Avoid creating definitions in the global name space.

The global namespace is the default namespace, where all functions, classes, constants, traits and interfaces live. The `global namespace <https://www.php.net/manual/en/language.namespaces.global.php>`_ is also known as the root namespace.

In particular, PHP native classes usually live in that namespace. By creating functions in that namespace, the code may encounter naming conflict, when the PHP group decides to use a name that the code also uses. This already happened in PHP version 5.1.1, where a ``Date`` native class was introduced, and had to be `disabled in the following minor version <https://www.php.net/ChangeLog-5.php#5.1.1>`_. 

Nowadays, conflicts appear between components, which claim the same name. 



.. code-block:: php
   
   <?php
   
   // This is not polluting the global namespace
   namespace My/Namespace {
   	class X {}
   }
   
   // This is polluting the global namespace
   // It might be in conflict with PHP classes in the future
   namespace {
   	class X {}
   }
   
   ?>

See also `Using namespaces: fallback to global function/constant <https://www.php.net/manual/en/language.namespaces.fallback.php>`_.

Connex PHP features
-------------------

  + `global-space <https://php-dictionary.readthedocs.io/en/latest/dictionary/global-space.ini.html>`_


Suggestions
___________

* Create a namespace for your code, and store your definition there.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/DontPolluteGlobalSpace                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


