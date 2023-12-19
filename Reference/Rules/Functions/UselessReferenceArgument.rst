.. _functions-uselessreferenceargument:

.. _useless-referenced-argument:

Useless Referenced Argument
+++++++++++++++++++++++++++

  The argument has a reference, but is only used for reading. 

This is probably a development artefact that was forgotten. It is better to remove it. 

This analysis also applies to `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loops, that declare the blind variable as reference, then use the variable as an object, accessing properties and methods. When a variable contains an object, there is no need to declare a reference : it is a reference automatically.


.. code-block:: php
   
   <?php
   
   function foo($a, &$b, &$c) {
       // $c is passed by reference, but only read. The reference is useless.
       $b = $c + $a;
       // The reference is useful for $b
   }
   
   foreach ($array as &$element) {
       $element->method();
   }
   
   ?>

See also `Objects and references <https://www.php.net/manual/en/language.oop5.references.php>`_.


Suggestions
___________

* Remove the useless & from the argument
* Make an actual use of the argument before the end of the method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UselessReferenceArgument                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | reference, argument                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-woocommerce-functions-uselessreferenceargument`, :ref:`case-magento-functions-uselessreferenceargument`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


