.. _typehints-couldbeparent:

.. _could-be-parent:

Could Be Parent
+++++++++++++++

.. meta::
	:description:
		Could Be Parent: Mark arguments, return types and properties that can be set to ``parent``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Parent
	:twitter:description: Could Be Parent: Mark arguments, return types and properties that can be set to ``parent``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Parent
	:og:type: article
	:og:description: Mark arguments, return types and properties that can be set to ``parent``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Parent.html
	:og:locale: en
Mark arguments, return types and properties that can be set to ``parent``.

This analysis works when typehints have already been configured.

.. code-block:: php
   
   <?php
   
   class x extends w {
       // Accept a w object as input 
       function foo(w $b) : w {
           // Returns a w object
           return $b;
       }   
   }
   
   ?>
Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Suggestions
___________

* Add `parent` typehint to the code.
* Add the literal class/type typehint to the code.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeParent                                                                                                 |
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


