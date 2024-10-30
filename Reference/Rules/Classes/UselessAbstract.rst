.. _classes-uselessabstract:

.. _useless-abstract-class:

Useless Abstract Class
++++++++++++++++++++++

  Those classes are marked 'abstract' and they are never extended. This way, they won't be instantiated nor used. 

Abstract classes that have only `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods are omitted here : one usage of such classes are Utilities classes, which only offer `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods.

.. code-block:: php
   
   <?php
   
   // Never extended class : this is useless
   abstract class foo {}
   
   // Extended class
   abstract class bar {
       public function barbar() {}
   }
   
   class bar2 extends bar {}
   
   // Utility class : omitted here
   abstract class bar {
       public static function barbar() {}
   }
   
   ?>
Connex PHP features
-------------------

  + `abstract <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract.ini.html>`_


Suggestions
___________

* Drop the abstract keyword
* Extends the abstract class, more than once
* If the class is extended, merge the class in the child




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UselessAbstract                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


