.. _traits-traitnotfound:

.. _trait-not-found:

Trait Not Found
+++++++++++++++

.. meta::
	:description:
		Trait Not Found: A unknown trait is mentioned in the use expression.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Trait Not Found
	:twitter:description: Trait Not Found: A unknown trait is mentioned in the use expression
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Trait Not Found
	:og:type: article
	:og:description: A unknown trait is mentioned in the use expression
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Trait Not Found.html
	:og:locale: en
A unknown trait is mentioned in the use expression. 

The used traits all exist, but in the configuration block, some unmentioned trait is called.

Be aware that the traits used in any configuration block may originate in any use expression. PHP will check the configuration block at instantiation only, and after compiling : at that moment, it will know all the used traits across the class.

.. code-block:: php
   
   <?php
   class x  { 
       // c is not a used trait
       use a, b { c::d insteadof e;}
   
       // e is a used trait, even if is not in the use above.
       use e;
   }
   ?>

See also `Traits <https://www.php.net/manual/en/language.oop5.traits.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Trait+%27a%27+not+found+.html>`_



Connex PHP features
-------------------

  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_


Suggestions
___________

* Switch the name of the trait to an existing and used trait
* Drop the expression that rely on the non-existent trait




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/TraitNotFound                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.9                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


