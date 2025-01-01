.. _complete-setparentdefinition:

.. _set-parent-definition:

Set Parent Definition
+++++++++++++++++++++

.. meta::
	:description:
		Set Parent Definition: This command creates a DEFINITION link between `parent` keyword and the actual parent class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Parent Definition
	:twitter:description: Set Parent Definition: This command creates a DEFINITION link between `parent` keyword and the actual parent class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Parent Definition
	:og:type: article
	:og:description: This command creates a DEFINITION link between `parent` keyword and the actual parent class
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Complete/SetParentDefinition.html
	:og:locale: en
This command creates a DEFINITION link between `parent` keyword and the actual `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class.

.. code-block:: php
   
   <?php
   
   class x { 
       const A = 1;
   }
   
   class y extends x {
       function foo() {
           // 'parent' needs a DEFFINITION link to the class x
           return parent::A;
       }
   }
   
   ?>

See also `Scope Resolution Operator (::) <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_.

Connex PHP features
-------------------

  + `parent <https://php-dictionary.readthedocs.io/en/latest/dictionary/parent.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetParentDefinition                                                                                                                                                            |
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


