.. _classes-useclassoperator:

.. _use-class-operator:

Use \:\:Class Operator
++++++++++++++++++++++

.. meta\:\:
	:description:
		Use \:\:Class Operator: Use ``\:\:class`` to hardcode class names, instead of strings.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use \:\:Class Operator
	:twitter:description: Use \:\:Class Operator: Use ``\:\:class`` to hardcode class names, instead of strings
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use \:\:Class Operator
	:og:type: article
	:og:description: Use ``\:\:class`` to hardcode class names, instead of strings
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/UseClassOperator.html
	:og:locale: en
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

Connex PHP features
-------------------

  + `class-operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-operator.ini.html>`_


Suggestions
___________

* Replace strings by the ::class operator whenever possible




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UseClassOperator                                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.7                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-typo3-classes-useclassoperator`                                                                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


