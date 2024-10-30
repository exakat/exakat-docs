.. _complete-enumcasevalues:

.. _enum-case-values:

Enum Case Values
++++++++++++++++

  Adds a `DEFINITION`link between a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ Enumeration case and its actual defined value. 

No link is added when no value is defined.

.. code-block:: php
   
   <?php
   
   enum E: string {
      case Foo = 'foo';
   }
   
   // Constants
   const C = E::Foo->name;  
   
   ?>
Connex PHP features
-------------------

  + `enum <https://php-dictionary.readthedocs.io/en/latest/dictionary/enum.ini.html>`_
  + `enum-backed <https://php-dictionary.readthedocs.io/en/latest/dictionary/enum-backed.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/EnumCaseValues                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


