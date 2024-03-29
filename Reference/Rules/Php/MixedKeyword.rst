.. _php-mixedkeyword:

.. _mixed-keyword:

Mixed Keyword
+++++++++++++

  Never becomes a PHP keyword. It is used for typing functions which never returns anything (either dies or throw an `exception) <https://www.php.net/exception>`_.

It should be avoided in classes, traits and interfaces. Methods, anonymous classes (sic), namespaces and functions are OK. 

Setting a `never` class in a namespaces doesn't make it legit.


.. code-block:: php
   
   <?php
   
   // This is OK
   function never() { } 
   
   // This is no OK
   class never {  } 
   
   ?>

See also `mixed <hhttps://www.php.net/manual/en/language.types.declarations.php#language.types.declarations.mixed>`_.


Suggestions
___________

* Rename the classes, traits and interfaces with a different name.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/MixedKeyword                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.0                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | mixed                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+


