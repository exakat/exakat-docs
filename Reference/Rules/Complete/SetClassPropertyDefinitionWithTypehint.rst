.. _complete-setclasspropertydefinitionwithtypehint:

.. _set-class-property-definition-with-typehint:

Set Class Property Definition With Typehint
+++++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Set Class Property Definition With Typehint: Links method call to its definition, thanks to property typehinting.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Class Property Definition With Typehint
	:twitter:description: Set Class Property Definition With Typehint: Links method call to its definition, thanks to property typehinting
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Class Property Definition With Typehint
	:og:type: article
	:og:description: Links method call to its definition, thanks to property typehinting
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Set Class Property Definition With Typehint.html
	:og:locale: en
Links method call to its definition, thanks to property typehinting. The link is ``DEFINITION``.

.. code-block:: php
   
   <?php
   
   class x {
       public x $p = null;
   
       public function bar() {
           return $this;
       }
   }
   
   $x = new x;
   
   // $x->p is of 'x' class
   $x->p->bar();
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetClassPropertyDefinitionWithTypehint                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                   |
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


