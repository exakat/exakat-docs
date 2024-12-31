.. _complete-setclassremotedefinitionwithlocalnew:

.. _set-class-remote-definition-with-local-new:

Set Class Remote Definition With Local New
++++++++++++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Set Class Remote Definition With Local New: Links method calls and properties to its definition, thanks to the local new.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Class Remote Definition With Local New
	:twitter:description: Set Class Remote Definition With Local New: Links method calls and properties to its definition, thanks to the local new
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Class Remote Definition With Local New
	:og:type: article
	:og:description: Links method calls and properties to its definition, thanks to the local new
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Complete/SetClassRemoteDefinitionWithLocalNew.html
	:og:locale: en
  Links method calls and properties to its definition, thanks to the local new. The link is ``DEFINITION``.

.. code-block:: php
   
   <?php
   
   class x {
       public function bar() {    }
   }
   
   function foo() {
       $a = new x;
       
       // This links to class x, method bar(), thanks to the local new.
       return $a->bar();
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetClassRemoteDefinitionWithLocalNew                                                                           |
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
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


