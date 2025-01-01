.. _complete-setclassremotedefinitionwithtypehint:

.. _set-class-remote-definition-with-typehint:

Set Class Remote Definition With Typehint
+++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Set Class Remote Definition With Typehint: Links method calls, properties static or not, and constants to their definition, thanks to typed arguments.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Class Remote Definition With Typehint
	:twitter:description: Set Class Remote Definition With Typehint: Links method calls, properties static or not, and constants to their definition, thanks to typed arguments
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Class Remote Definition With Typehint
	:og:type: article
	:og:description: Links method calls, properties static or not, and constants to their definition, thanks to typed arguments
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Complete/SetClassRemoteDefinitionWithTypehint.html
	:og:locale: en
Links method calls, properties `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or not, and constants to their definition, thanks to typed arguments. The link is ``DEFINITION``.

.. code-block:: php
   
   <?php
   
   class x {
       public function bar() {    }
   }
   
   function foo(x $a) {
       // This links to class x, method bar(), thanks to the typehint.
       return $a->bar();
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetClassRemoteDefinitionWithTypehint                                                                           |
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


