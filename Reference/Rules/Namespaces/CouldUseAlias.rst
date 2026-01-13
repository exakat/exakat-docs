.. _namespaces-couldusealias:

.. _could-use-alias:

Could Use Alias
+++++++++++++++

  This long name may be reduced by using an available alias.

This applies to classes (as full name or prefix), and to constants and functions.

.. code-block:: php
   
   <?php
   
   use a\b\c;
   use function a\b\c\foo;
   use const a\b\c\D;
   
   // This may be reduced with the above alias to c\d()
   new a\b\c\d();
   
   // This may be reduced to c\d\e\f 
   new a\b\c\d\e\f();
   
   // This may be reduced to c()
   new a\b\c();
   
   // This may be reduced to D
   echo a\b\c\D;
   
   // This may be reduced to D
   a\b\c\foo();
   
   // This can't be reduced : it is an absolute name
   \a\b\c\foo();
   
   // This can't be reduced : it is no an alias nor a prefix
   a\b\d\foo();
   
   ?>

See also `Using namespaces: Aliasing/Importing ¶ <https://www.php.net/manual/en/language.namespaces.importing.php>`_.

Connex PHP features
-------------------

  + `namespace <https://php-dictionary.readthedocs.io/en/latest/dictionary/namespace.ini.html>`_
  + `use-alias <https://php-dictionary.readthedocs.io/en/latest/dictionary/use-alias.ini.html>`_


Suggestions
___________

* Use all your aliases so as to make the code shorter and more readable
* Add new aliases for missing path
* Make class names absolute and drop the aliases




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/CouldUseAlias                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
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


