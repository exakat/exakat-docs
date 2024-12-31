.. _traits-unusedtrait:

.. _unused-traits:

Unused Traits
+++++++++++++

.. meta\:\:
	:description:
		Unused Traits: Those traits are not used in any class or trait.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Traits
	:twitter:description: Unused Traits: Those traits are not used in any class or trait
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Traits
	:og:type: article
	:og:description: Those traits are not used in any class or trait
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Traits/UnusedTrait.html
	:og:locale: en
  Those traits are not used in any class or trait. They are probably dead code, as there is no way to use a trait without a host class.

.. code-block:: php
   
   <?php
   
   // unused trait
   trait unusedTrait { /**/ }
   
   // used trait
   trait tUsedInTrait { /**/ }
   
   trait tUsedInClass { 
       use tUsedInTrait;
       /**/ 
       }
   
   class foo {
       use tUsedInClass;
   }
   ?>
Connex PHP features
-------------------

  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_


Suggestions
___________

* Remove the unused trait
* Actually use the trait in one class or another trait




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/UnusedTrait                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


