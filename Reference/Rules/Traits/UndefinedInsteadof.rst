.. _traits-undefinedinsteadof:

.. _undefined-insteadof:

Undefined Insteadof
+++++++++++++++++++

.. meta::
	:description:
		Undefined Insteadof: ``Insteadof`` tries to replace a method with another, but it doesn't exists.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Undefined Insteadof
	:twitter:description: Undefined Insteadof: ``Insteadof`` tries to replace a method with another, but it doesn't exists
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Undefined Insteadof
	:og:type: article
	:og:description: ``Insteadof`` tries to replace a method with another, but it doesn't exists
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Traits/UndefinedInsteadof.html
	:og:locale: en
``Insteadof`` tries to replace a method with another, but it doesn't exists. This happens when the replacing class is refactored, and some of its definition are dropped. 

``Insteadof`` may replace a non-existing method with an existing one, but not the contrary. 



This `error <https://www.php.net/error>`_ is not linted : it only appears at execution time.

.. code-block:: php
   
   <?php
   
   trait A {
       function C (){}
   }
   
   trait B {
       function C (){}
   }
   
   class Talker {
       use A, B {
           B::C insteadof A;
           B::D insteadof A;
       }
   }
   
   new Talker();
   ?>

See also `Traits <https://www.php.net/manual/en/language.oop5.traits.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/An+alias+%28%25s%29+was+defined+for+method+%25s%28%29%2C+but+this+method+does+not+exist.html>`_



Connex PHP features
-------------------

  + `insteadof <https://php-dictionary.readthedocs.io/en/latest/dictionary/insteadof.ini.html>`_
  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_
  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Suggestions
___________

* Remove the insteadof expression
* Fix the original method and replace it with an existing method




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/UndefinedInsteadof                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.2                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


