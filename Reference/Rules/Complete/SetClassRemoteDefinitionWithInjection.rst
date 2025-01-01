.. _complete-setclassremotedefinitionwithinjection:

.. _set-class-remote-definition-with-injection:

Set Class Remote Definition With Injection
++++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Set Class Remote Definition With Injection: Links a method call and its definition, thanks to a typehint.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Class Remote Definition With Injection
	:twitter:description: Set Class Remote Definition With Injection: Links a method call and its definition, thanks to a typehint
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Class Remote Definition With Injection
	:og:type: article
	:og:description: Links a method call and its definition, thanks to a typehint
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Complete/SetClassRemoteDefinitionWithInjection.html
	:og:locale: en
Links a method call and its definition, thanks to a typehint.

.. code-block:: php
   
   <?php
   
   class A {
       function goo() {}
   }
   
   function foo(A $arg) {
       // This goes to method A::goo(), thanks to the typehint
       $arg->goo();
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetClassRemoteDefinitionWithInjection                                                                          |
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


