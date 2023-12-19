.. _constants-multipleconstantdefinition:

.. _multiple-constant-definition:

Multiple Constant Definition
++++++++++++++++++++++++++++

  Some constants are defined several times in your code. This will lead to a fatal `error <https://www.php.net/error>`_, if they are defined during the same execution. 

Multiple definitions may happens at bootstrap, when the application code is collecting information about the current environment. It may also happen at inclusion time, which one set of constant being loaded, while other definition are not, avoiding conflict. Both are false positive. 


.. code-block:: php
   
   <?php
   
   // OS is defined twice. 
   if (PHP_OS == 'Windows') {
       define('OS', 'Win');
   } else {
       define('OS', 'Other');
   }
   
   ?>

See also `class <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.class>`_.


Suggestions
___________

* Move the constants to a class, and include the right class based on control flow.
* Give different names to the constants, and keep the condition close to utilisation.
* Move the constants to an external configuration file : it will be easier to identify that those constants may change.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/MultipleConstantDefinition                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
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
| Features     | class                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolibarr-constants-multipleconstantdefinition`, :ref:`case-openconf-constants-multipleconstantdefinition`                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


