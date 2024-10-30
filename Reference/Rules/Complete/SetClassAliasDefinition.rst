.. _complete-setclassaliasdefinition:

.. _set-class\_alias()-definition:

Set class_alias() Definition
++++++++++++++++++++++++++++

  Links identifiers and nsname to the concrete class, interface, trait and enumeration when `class_alias() <https://www.php.net/class_alias>`_ was used to create the name. The link is ``DEFINITION``.

`class_alias() <https://www.php.net/class_alias>`_ are detected at loading time, and are used unconditionally.

This means that the fully qualified name of the ``new`` call and the instantiated class may be different : without the alias, the fully qualified name is the current value, or its use's origin, while with `class_alias() <https://www.php.net/class_alias>`_, it is an arbitrary name.

.. code-block:: php
   
   <?php
   
   class x {
       public function foo() {}
   }
   
   class_alias('x', 'y');
   
   //y exists, as an alias of x.
   $y = new y;
   
   ?>
Connex PHP features
-------------------

  + `class-alias <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-alias.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetClassAliasDefinition                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`NoDoc <ruleset-NoDoc>`                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


