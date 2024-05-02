.. _classes-couldbestringable:

.. _could-be-stringable:

Could Be Stringable
+++++++++++++++++++

  ``Stringable`` is an interface that marks classes with a custom method to cast the object as a string. It was introduced in PHP 8.0.

Classes that defined a `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_ magic method may be turned into a string when the typehint, argument, return or property, requires it. This is not the case when strict_types is activated. Yet, until PHP 8.0, there was nothing to identify a class as such.

.. code-block:: php
   
   <?php 
   
   // This class may implement Stringable
   class x {
       function __tostring() {
           return 'asd';
       }
   }
   
   echo (new x);
   
   ?>

See also `PHP RFC: Add Stringable interface <https://wiki.php.net/rfc/stringable>`_ and `The Stringable interface <https://www.php.net/manual/en/class.stringable.php>`_.


Suggestions
___________

* Add implements stringable to the class definition
* Add extends stringable to the interface definition




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeStringable                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | stringable, string, magic-method                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


