.. _classes-emptyclass:

.. _empty-classes:

Empty Classes
+++++++++++++

  Classes that do no define anything at all : no property, method nor constant. This is possibly dead code.

Empty classes are sometimes used to group classes; an interface may be used here for the same purpose, without inserting an extra level in the class hierarchy.


.. code-block:: php
   
   <?php
   
   //Empty class
   class foo extends bar {}
   
   //Not an empty class
   class foo2 extends bar {
       const FOO = 2;
   }
   
   //Not an empty class, as derived from Exception
   class barException extends \Exception {}
   
   ?>


Classes that are directly derived from an `exception <https://www.php.net/exception>`_ are omitted.

See also `class <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.class>`_.


Suggestions
___________

* Remove the empty class: it is possibly dead code.
* Add some code to the class to make it concrete.
* Turn the class into an interface.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/EmptyClass                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | class                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-classes-emptyclass`                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


