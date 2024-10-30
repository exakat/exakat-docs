.. _variables-staticvariables:

.. _static-variables:

Static Variables
++++++++++++++++

  PHP variables may be `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or standard. `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables survive after the function execution end, and are available at the next function run. They are distinct from globals, which are available application wide, and from `static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties, which are tied to a class. `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables are tied to a function, method, `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_ or arrow function.

.. code-block:: php
   
   <?php
   
   function foo() {
       // static variable
       static $count = 0;
       
       echo ++$count;
   }
   
   class bar {
       // This is not a static variable : 
       // it is a static property
       static $property = 1;
   }
   
   ?>

See also `Using static variables <https://www.php.net/manual/en/language.variables.scope.php#language.variables.scope.static>`_.

Connex PHP features
-------------------

  + `static-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/static-variable.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/StaticVariables                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


