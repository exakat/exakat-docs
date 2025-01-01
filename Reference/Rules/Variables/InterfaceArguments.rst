.. _variables-interfacearguments:

.. _interface-arguments:

Interface Arguments
+++++++++++++++++++

.. meta::
	:description:
		Interface Arguments: This rule lists variables that are arguments in an interface.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Interface Arguments
	:twitter:description: Interface Arguments: This rule lists variables that are arguments in an interface
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Interface Arguments
	:og:type: article
	:og:description: This rule lists variables that are arguments in an interface
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Variables/InterfaceArguments.html
	:og:locale: en
This rule lists variables that are arguments in an interface.

.. code-block:: php
   
   <?php
   
   interface i {
       function interfaceMethod($interfaceArgument) ;
   }
   
   class foo extends i {
       // Save function as above, but the variable is not reported
       function interfaceMethod($notAnInterfaceArgument) {}
   }
   
   ?>
Connex PHP features
-------------------

  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/InterfaceArguments                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
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


