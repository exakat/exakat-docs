.. _classes-useclassoperator:

.. _use-class-operator:

Use \:\:Class Operator
++++++++++++++++++++++

  Use ``\:\:class`` to hardcode class names, instead of strings.

This is actually faster than strings, which are parsed at execution time, while ``\:\:class`` is compiled, making it faster to execute. 

``\:\:class`` operator is also able to handle use expressions, including aliases and local namespace. The code is easier to maintain. For example, the target class's namespace may be renamed, without changing the ``\:\:class``, while the string must be updated.

``\:\:class`` operator works with ``self`` and ``static``keywords. 
This is not possible when building the name of the class with concatenation.

This is a micro-optimization. This also helps `static <https://www.php.net/manual/en/language.oop5.static.php>`_ analysis, as it gives more information at compile time to analyse.

.. code-block:: php
   
   <?php
   
   namespace foo\bar;
   
   use foo\bar\X as B;
   
   class X {}
   
   $className = '\foo\bar\X';
   
   $className = foo\bar\X::class;
   
   $className = B\X;
   
   $object = new $className;
   
   ?>

See also `::class <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.class.class>`_.


Suggestions
___________

* Replace strings by the ::class operator whenever possible




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UseClassOperator                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Performances <ruleset-Performances>`                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.7                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | class-operator                                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-typo3-classes-useclassoperator`                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


