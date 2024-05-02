.. _functions-deprecatedcallable:

.. _deprecated-callable:

Deprecated Callable
+++++++++++++++++++

  Callable functions that are supported by ``call_user_func($callable)``, but not with the ``$callable()`` syntax are deprecated. 

One important aspect is the loss of context : 'self\:\:method' may be created anywhere in the code, while `self\:\:class` can only be used inside a class, and, in that case, inside the target class. 
It is recommended to update the code with any PHP version, to prepare for the future removal of the feature.

.. code-block:: php
   
   <?php
   
   class x {
       // This will fail 
       function foo(callable $callable) {
           $callable();
       }
       
       function method() {
       
       }
   }
   
   $x = new x;
   $x->foo('self::method');
   ?>

See also `PHP RFC: Deprecate partially supported callables <https://wiki.php.net/rfc/deprecate_partially_supported_callables>`_.


Suggestions
___________

* Replace the keyword (such as self) by the full class name, with self::class.
* Use a variable and the $s(...) syntax.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/DeprecatedCallable                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.1                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.2 and older                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------+
| Features     | callable                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------+


