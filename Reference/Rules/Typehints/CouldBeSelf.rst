.. _typehints-couldbeself:

.. _could-be-self:

Could Be Self
+++++++++++++

.. meta::
	:description:
		Could Be Self: Mark arguments, return types and properties that can be set to ``self``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Self
	:twitter:description: Could Be Self: Mark arguments, return types and properties that can be set to ``self``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Self
	:og:type: article
	:og:description: Mark arguments, return types and properties that can be set to ``self``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Typehints/CouldBeSelf.html
	:og:locale: en
Mark arguments, return types and properties that can be set to ``self``. This applies only to methods. 

This analysis works when typehints have already been configured.

.. code-block:: php
   
   <?php
   
   class x {
       // Accept a x object as input 
       function foo(x $b) : x {
           // Returns a x object
           return $b;
       }   
   }
   
   ?>
Connex PHP features
-------------------

  + `self <https://php-dictionary.readthedocs.io/en/latest/dictionary/self.ini.html>`_


Suggestions
___________

* Add `self` typehint to the code.
* Add the literal class/type typehint to the code.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeSelf                                                                                                   |
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


