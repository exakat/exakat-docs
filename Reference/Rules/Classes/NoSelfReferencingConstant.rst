.. _classes-noselfreferencingconstant:

.. _no-self-referencing-constant:

No Self Referencing Constant
++++++++++++++++++++++++++++

  It is not possible to use a constant to define itself in a class. It yields a fatal `error <https://www.php.net/error>`_ at runtime. 

The PHP `error <https://www.php.net/error>`_ reads : ``Cannot declare `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_-referencing constant 'self\:\:C2'``. Unlike PHP which is `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_-referencing, `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ referencing variables can't have a value : just don't use that.
The code may access an already declared constant with `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ or with its class name.
This `error <https://www.php.net/error>`_ is not detected by linting. It is only detected at instantiation time : if the class is not used, it won't appear.

.. code-block:: php
   
   <?php
       class a { 
           const C1 = 1;         // fully defined constant
           const C2 = self::C2;  // self referencing constant
           const C3 = a::C3 + 2; // self referencing constant
       }
   ?>

Suggestions
___________

* Give a literal value to this constant
* Give a constant value to this constant : other class constants or constant are allowed here.




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NoSelfReferencingConstant                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | constant                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


