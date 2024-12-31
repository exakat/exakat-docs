.. _functions-wrongreturnedtype:

.. _wrong-type-returned:

Wrong Type Returned
+++++++++++++++++++

.. meta\:\:
	:description:
		Wrong Type Returned: The returned value is not compatible with the specified return type.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong Type Returned
	:twitter:description: Wrong Type Returned: The returned value is not compatible with the specified return type
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong Type Returned
	:og:type: article
	:og:description: The returned value is not compatible with the specified return type
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/WrongReturnedType.html
	:og:locale: en
  The returned value is not compatible with the specified return type.

.. code-block:: php
   
   <?php
   
   // classic error
   function bar() : int {
       return 'A';
   }
   
   // classic static error
   const B = 2;
   function bar() : string {
       return B;
   }
   
   // undecideable error
   function bar($c) : string {
       return $c;
   }
   
   // PHP lint this, but won't execute it
   function foo() : void {
       // No return at all 
   }
   
   ?>

See also `Returning values <https://www.php.net/manual/en/functions.returning-values.php>`_, `Void Return Type <https://wiki.php.net/rfc/void_return_type>`_, :ref:`Mismatch Type And Default <mismatch-type-and-default>` and :ref:`Wrong Typed Property Default <wrong-typed-property-default>`.


Suggestions
___________

* Match the return type with the return value
* Remove the return expression altogether
* Add a typecast to the returning expression




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/WrongReturnedType                                                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.7                                                                                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


