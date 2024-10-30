.. _classes-wrongtypedpropertyinit:

.. _wrong-typed-property-default:

Wrong Typed Property Default
++++++++++++++++++++++++++++

  Property is typed, yet receives an incompatible value at constructor time.

Initialized type might be a new instance, the return of a method call or an interface compatible object.



PHP compiles such code, but won't execute it, as it detects the incompatibility at execution time.

.. code-block:: php
   
   <?php
   
   class x {
       private A $property;
       private B $incompatible;
       
       function __construct() {
           // This is compatible
           $this->property = new A();
           
           // This is incompatible : new B() expected
           $this->incompatible = new C();
           
       }
   }
   
   ?>

See also :ref:`Wrong Type Returned <wrong-type-returned>` and :ref:`Mismatch Type And Default <mismatch-type-and-default>`.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Cannot+use+int+as+default+value+for+parameter+%24a+of+type+string.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/Cannot+use+int+as+default+value+for+property+x%3A%3A%24a+of+type+string.html>`_



Connex PHP features
-------------------

  + `default-value <https://php-dictionary.readthedocs.io/en/latest/dictionary/default-value.ini.html>`_


Suggestions
___________

* Remove the type hint of the property
* Fix the initialization call
* Use an interface for typehint




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/WrongTypedPropertyInit                                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.9                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and more recent                                                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


