.. _typehints-couldbevoid:

.. _could-be-void:

Could Be Void
+++++++++++++

.. meta::
	:description:
		Could Be Void: Mark return types that can be set to void.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Void
	:twitter:description: Could Be Void: Mark return types that can be set to void
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Void
	:og:type: article
	:og:description: Mark return types that can be set to void
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Typehints/CouldBeVoid.html
	:og:locale: en
Mark return types that can be set to void.
All abstract methods (in classes or in interfaces) are omitted here.

.. code-block:: php
   
   <?php
   
   // No return, this should be void.
   function foo() {
       ++$a; // Not useful
   }
   
   ?>
Connex PHP features
-------------------

  + `void <https://php-dictionary.readthedocs.io/en/latest/dictionary/void.ini.html>`_


Suggestions
___________

* Add the void typehint to the code.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeVoid                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


