.. _functions-isgenerator:

.. _method-is-a-generator:

Method Is A Generator
+++++++++++++++++++++

  This rule marks functions, methods, `... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_ that are using ``yield`` and ``yield from`` keywords. The usage of that keyword makes them `Generator <https://www.php.net/manual/en/class.`generator <https://www.php.net/generator>`_.php>`_, as is show by the compulsory return type of ``Generator``.

.. code-block:: php
   
   <?php
   
   function generator() {
       yield from generator2();
       
       return 3;
   }
   
   function generator2() {
       yield 1;
       yield 2;
   }
   
   ?>

See also `Generators overview <https://www.php.net/manual/en/language.generators.overview.php>`_.

Connex PHP features
-------------------

  + `generator <https://php-dictionary.readthedocs.io/en/latest/dictionary/generator.ini.html>`_
  + `yield <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield.ini.html>`_
  + `yield-from <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield-from.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/IsGenerator                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


