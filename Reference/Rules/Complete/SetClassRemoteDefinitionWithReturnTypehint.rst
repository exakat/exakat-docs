.. _complete-setclassremotedefinitionwithreturntypehint:

.. _set-class-remote-definition-with-return-typehint:

Set Class Remote Definition With Return Typehint
++++++++++++++++++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Set Class Remote Definition With Return Typehint: Links method call to its definition, thanks to the typed return.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Class Remote Definition With Return Typehint
	:twitter:description: Set Class Remote Definition With Return Typehint: Links method call to its definition, thanks to the typed return
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Class Remote Definition With Return Typehint
	:og:type: article
	:og:description: Links method call to its definition, thanks to the typed return
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Complete/SetClassRemoteDefinitionWithReturnTypehint.html
	:og:locale: en
  Links method call to its definition, thanks to the typed return. The link is ``DEFINITION``.

.. code-block:: php
   
   <?php
   
   class x {
       public function bar() {    }
   }
   
   function foo() {
       $a = bar();
       // This links to class x, method bar(), thanks to the new.
       return $a->bar();
   }
   
   function bar() : x {
       return new x;
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetClassRemoteDefinitionWithReturnTypehint                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


