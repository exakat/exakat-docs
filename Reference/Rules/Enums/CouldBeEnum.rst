.. _enums-couldbeenum:

.. _could-be-enumeration:

Could Be Enumeration
++++++++++++++++++++

.. meta::
	:description:
		Could Be Enumeration: This rule detects a potential enumeration.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Enumeration
	:twitter:description: Could Be Enumeration: This rule detects a potential enumeration
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Enumeration
	:og:type: article
	:og:description: This rule detects a potential enumeration
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Enumeration.html
	:og:locale: en
This rule detects a potential enumeration. When a property is only and ever assigned a finite number of literals, it may be turned into an enumeration.
Currently, the analysis focuses on properties that may have 2 or more values (parameter `minElements`). The property should only be assigned literals, or constants.

.. code-block:: php
   
   <?php
   
   class x {
       private $p = 0;
       
       function foo() {
           if ($this->p === 0) {
               $this->p = 1;
           } else {
               $this->p = 0;
           }
       }
   }
   
   ?>

+-------------+---------+---------+-------------------------------------------------------------------------------+
| Name        | Default | Type    | Description                                                                   |
+-------------+---------+---------+-------------------------------------------------------------------------------+
| minElements | 2       | integer | Minimal number of elements to consider that a property may be an enumeration. |
+-------------+---------+---------+-------------------------------------------------------------------------------+



Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Enums/CouldBeEnum                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | 8.1                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


