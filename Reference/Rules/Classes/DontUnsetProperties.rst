.. _classes-dontunsetproperties:

.. _don't-unset-properties:

Don't Unset Properties
++++++++++++++++++++++

  Don't unset properties. They would go undefined, and raise warnings of undefined properties, even though the property is explicitly defined in the original class. 

When getting rid of a property, assign it to `null`. This keeps the property defined in the object, yet allows existence check without errors.
This analysis works on properties and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties. It also reports magic properties being unset.

Thanks for `Benoit Burnichon <https://twitter.com/BenoitBurnichon>`_ for the original idea.

.. code-block:: php
   
   <?php
   
   class Foo {
       public $a = 1;
   }
   
   $a = new Foo();
   
   var_dump((array) $a) ;
   // la propriété est reportée, et null
   // ['a' => null]
   
   unset($a->a);
   
   var_dump((array) $a) ;
   //Empty []
   
   // Check if a property exists
   var_dump($a->b === null);
   
   // Same result as above, but with a warning
   var_dump($a->c === null);
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Undefined+property.html>`_



Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Suggestions
___________

* Set the property to null or its default value
* Make the property an array, and set/unset its index




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DontUnsetProperties                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Top10 <ruleset-Top10>`, :ref:`php-cs-fixable <ruleset-php-cs-fixable>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.3                                                                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-vanilla-classes-dontunsetproperties`, :ref:`case-typo3-classes-dontunsetproperties`                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


