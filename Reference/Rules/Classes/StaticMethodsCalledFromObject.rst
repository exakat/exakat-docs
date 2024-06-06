.. _classes-staticmethodscalledfromobject:

.. _static-methods-called-from-object:

Static Methods Called From Object
+++++++++++++++++++++++++++++++++

  `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods may be called without instantiating an object. As such, they never interact with the special variable '`$this <https://www.php.net/manual/en/language.oop5.basic.php>`_', as they do not depend on object existence. 

Besides this, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods are normal methods that may be called directly from object context, to perform some utility task. 

To maintain code readability, it is recommended to call `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method in a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ way, rather than within object context.

.. code-block:: php
   
   <?php
       class x {
           static function y( ) {}
       }
       
       $z = new x( );
       
       $z->y( ); // Readability : no one knows it is a static call
       x::y( );  // Readability : here we know
   ?>

Suggestions
___________

* Switch to static method syntax
* Remove the static option from the method




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/StaticMethodsCalledFromObject                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | object, static                                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


