.. _functions-modifytypedparameter:

.. _modified-typed-parameter:

Modified Typed Parameter
++++++++++++++++++++++++

.. meta::
	:description:
		Modified Typed Parameter: Reports modified parameters, which have a non-scalar typehint.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Modified Typed Parameter
	:twitter:description: Modified Typed Parameter: Reports modified parameters, which have a non-scalar typehint
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Modified Typed Parameter
	:og:type: article
	:og:description: Reports modified parameters, which have a non-scalar typehint
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Modified Typed Parameter.html
	:og:locale: en
Reports modified parameters, which have a non-scalar typehint. Such variables should not be changed within the body of the method. Unlike typed properties, which always hold the expected type, typed parameters are only guaranteed type at the beginning of the method block. 
This problem doesn't apply to scalar types : by default, PHP pass scalar parameters by value, not by reference. Class types are always passed by reference.

This problem is similar to :ref:`don't-unset-properties`  : the `static <https://www.php.net/manual/en/language.oop5.static.php>`_ specification of the property may be unset, leading to confusing 'undefined property', while the class hold the property definition.

.. code-block:: php
   
   <?php
   
   class x {
   
       function foo(Y $y) {
           // $y is type Y
   
           // A cast version of $y is stored into $yAsString. $y is untouched.
           $yAsString = (string) $y;
   
           // $y is of type 'int', now.
           $y = 1;
   
           // Some more code
   
           // display the string version.
           echo $yAsString; 
           // so, Y $y is now raising an error
           echo $y->name; 
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_
  + `parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/parameter.ini.html>`_


Suggestions
___________

* Use different variable names when converting a parameter to a different type.
* Only use methods and properties calls on a typed parameter.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/ModifyTypedParameter                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


