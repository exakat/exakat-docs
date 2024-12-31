.. _complete-setclassremotedefinitionwithparenthesis:

.. _set-class-remote-definition-with-parenthesis:

Set Class Remote Definition With Parenthesis
++++++++++++++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Set Class Remote Definition With Parenthesis: Links methodcall, properties and constants to its definition, based to the new in the parenthesis.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Class Remote Definition With Parenthesis
	:twitter:description: Set Class Remote Definition With Parenthesis: Links methodcall, properties and constants to its definition, based to the new in the parenthesis
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Class Remote Definition With Parenthesis
	:og:type: article
	:og:description: Links methodcall, properties and constants to its definition, based to the new in the parenthesis
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Complete/SetClassRemoteDefinitionWithParenthesis.html
	:og:locale: en
  Links methodcall, properties and constants to its definition, based to the new in the parenthesis. The link is ``DEFINITION``.

.. code-block:: php
   
   <?php
   
   class x {
       public function bar() {    }
   }
   
   function foo() {
       // This links to class x, method bar(), thanks to the new.
       return (new x)->bar();
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetClassRemoteDefinitionWithParenthesis                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`NoDoc <ruleset-NoDoc>`                                                                  |
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


