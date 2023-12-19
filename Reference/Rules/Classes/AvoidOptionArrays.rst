.. _classes-avoidoptionarrays:

.. _avoid-option-arrays-in-constructors:

Avoid option arrays in constructors
+++++++++++++++++++++++++++++++++++

  Avoid option arrays in constructors. Use one parameter per injected element.


.. code-block:: php
   
   <?php
   
   class Foo {
       // Distinct arguments, all typehinted if possible
       function __construct(A $a, B $b, C $c, D $d) {
           $this->a = $a;
           $this->b = $b;
           $this->c = $c;
           $this->d = $d;
       }
   }
   
   class Bar {
       // One argument, spread over several properties
       function __construct(array $options) {
           $this->a = $options['a'];
           $this->b = $options['b'];
           $this->c = $options['c'];
           $this->d = $options['d'];
       }
   }
   
   ?>

See also `Avoid option arrays in constructors <http://bestpractices.thecodingmachine.com/php/design_beautiful_classes_and_methods.html#avoid-option-arrays-in-constructors>`_ and `PHP RFC: Named Arguments (Type-safe and documented options) <https://wiki.php.net/rfc/named_params#type-safe_and_documented_options>`_.


Suggestions
___________

* Spread the options in the argument list, one argument each
* Use a configuration class, that hold all the elements with clear names, instead of an array
* Use named parameters to pass and document the arguments




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/AvoidOptionArrays                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | constructor                                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


