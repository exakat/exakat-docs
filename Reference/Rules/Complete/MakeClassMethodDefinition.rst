.. _complete-makeclassmethoddefinition:

.. _make-class-method-definition:

Make Class Method Definition
++++++++++++++++++++++++++++

.. meta::
	:description:
		Make Class Method Definition: This command links a method call to its method definition.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Make Class Method Definition
	:twitter:description: Make Class Method Definition: This command links a method call to its method definition
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Make Class Method Definition
	:og:type: article
	:og:description: This command links a method call to its method definition
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Make Class Method Definition.html
	:og:locale: en
This command links a method call to its method definition. 
This command may not detect all possible link for the methods. It may be missing information about the nature of the object.

This command may also produce multiple definitions link, when the definition are ambiguous.

.. code-block:: php
   
   <?php
   
   class x {
       function foo() {
           // This links to the bar() method
           return $this->bar();
       }
   
       function bar() {
           // This links to the link() method
           return $this->bar();
       }
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/MakeClassMethodDefinition                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


