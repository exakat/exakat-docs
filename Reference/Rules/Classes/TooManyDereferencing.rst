.. _classes-toomanydereferencing:

.. _too-many-dereferencing:

Too Many Dereferencing
++++++++++++++++++++++

  Linking too many properties and methods, one to the other.

This analysis counts both `static <https://www.php.net/manual/en/language.oop5.static.php>`_ calls and normal call; methods, properties and constants. It also takes into account arrays along the way.

The default limit of chaining methods and properties is set to 7 by default. 
Too many chained methods is harder to read.

.. code-block:: php
   
   <?php
   
   // 9 chained calls.
   $main->getA()->getB()->getC()->getD()->getE()->getF()->getG()->getH()->getI()->property;
   
   ?>

+----------------------+---------+---------+----------------------------------+
| Name                 | Default | Type    | Description                      |
+----------------------+---------+---------+----------------------------------+
| tooManyDereferencing | 7       | integer | Maximum number of dereferencing. |
+----------------------+---------+---------+----------------------------------+


Connex PHP features
-------------------

  + `dereferencing <https://php-dictionary.readthedocs.io/en/latest/dictionary/dereferencing.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/TooManyDereferencing                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.7                                                                                                                   |
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


