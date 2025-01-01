.. _traits-undefinedtrait:

.. _undefined-trait:

Undefined Trait
+++++++++++++++

.. meta::
	:description:
		Undefined Trait: Those are undefined, traits .
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Undefined Trait
	:twitter:description: Undefined Trait: Those are undefined, traits 
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Undefined Trait
	:og:type: article
	:og:description: Those are undefined, traits 
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Traits/UndefinedTrait.html
	:og:locale: en
Those are undefined, traits . 

When the using class or trait is instantiated, PHP emits a a fatal `error <https://www.php.net/error>`_.

Trait which are referenced in a `use` expression are omitted: they are considered part of code that is probably outside the current code, either omitted or in external component.

.. code-block:: php
   
   <?php
   
   use Composer/Component/someTrait as externalTrait;
   
   trait t {
       function foo() {}
   }
   
   // This class uses trait that are all known
   class hasOnlyDefinedTrait {
       use t, externalTrait;
   }
   
   // This class uses trait that are unknown
   class hasUndefinedTrait {
       use unknownTrait, t, externalTrait;
   }
   ?>
Related PHP errors 
-------------------

  + `Trait '%s' not found <https://php-errors.readthedocs.io/en/latest/messages/Trait+%27T%27+not+found.html>`_




Suggestions
___________

* Define the missing trait
* Remove usage of the missing trait




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/UndefinedTrait                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


