.. _functions-noclassastypehint:

.. _no-class-as-typehint:

No Class As Typehint
++++++++++++++++++++

  Avoid using concrete classes as typehint : always use interfaces or abstract classes. This way, different classes, or versions of classes may be passed as argument. The typehint is not linked to an implementation, but to signatures.

A class is needed when the object is with properties : interfaces do not allow the specifications of properties.

.. code-block:: php
   
   <?php
   
   class X {
       public $p = 1;
   
       function foo() {}
   }
   
   interface i {
       function foo();
   }
   
   // X is a class : any update in the code requires changing / subclassing X or the rest of the code.
   function bar(X $x) {
       $x->foo();
   }
   
   // I is an interface : X may implements this interface without refactoring and pass
   // later, newer versions of X may get another name, but still implement I, and still pass
   function bar2(I $x) {
       $x->foo();
   }
   
   function bar3(I $x) {
       echo $x->p;
   }
   
   ?>

See also `Type hinting for interfaces <http://phpenthusiast.com/object-oriented-php-tutorials/type-hinting-for-interfaces>`_.

Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_
  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Create an interface with the important methods, and use that interface
* Create an abstract class, when public properties are also needed




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NoClassAsTypehint                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.4                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-vanilla-functions-noclassastypehint`, :ref:`case-phpmyadmin-functions-noclassastypehint`                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


