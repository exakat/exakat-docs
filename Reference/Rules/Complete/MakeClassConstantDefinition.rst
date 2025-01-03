.. _complete-makeclassconstantdefinition:

.. _makes-class-constant-definition:

Makes Class Constant Definition
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		Makes Class Constant Definition: This rule adds DEFINITION link between class constant definitions and their usage.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Makes Class Constant Definition
	:twitter:description: Makes Class Constant Definition: This rule adds DEFINITION link between class constant definitions and their usage
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Makes Class Constant Definition
	:og:type: article
	:og:description: This rule adds DEFINITION link between class constant definitions and their usage
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Makes Class Constant Definition.html
	:og:locale: en
This rule adds DEFINITION link between class constant definitions and their usage. These links are used later to identify the values delivered by the constant.

.. code-block:: php
   
   <?php
   
   class x {
       public const A = 1;
   }
   
   // Link to the constant definition
   echo x::A;
   
   // Cannot find the original class
   echo $x::A;
   
   ?>
Connex PHP features
-------------------

  + `class-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/MakeClassConstantDefinition                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


