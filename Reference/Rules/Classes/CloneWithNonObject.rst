.. _classes-clonewithnonobject:

.. _clone-with-non-object:

Clone With Non-Object
+++++++++++++++++++++

.. meta::
	:description:
		Clone With Non-Object: The ``clone`` keyword must be used on variables, properties or results from a function or method call.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Clone With Non-Object
	:twitter:description: Clone With Non-Object: The ``clone`` keyword must be used on variables, properties or results from a function or method call
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Clone With Non-Object
	:og:type: article
	:og:description: The ``clone`` keyword must be used on variables, properties or results from a function or method call
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/CloneWithNonObject.html
	:og:locale: en
The ``clone`` keyword must be used on variables, properties or results from a function or method call. 

``clone`` cannot be used with constants or literals.
Cloning a non-object lint but won't execute.

.. code-block:: php
   
   <?php
   
   class x { }
   $x = new x();
   
   // Valid clone
   $y = clone $x;
   
   // Invalid clone
   $y = clone x;
   
   ?>

See also `Object cloning <https://www.php.net/manual/en/language.oop5.cloning.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/__clone+method+called+on+non-object.html>`_



Connex PHP features
-------------------

  + `clone <https://php-dictionary.readthedocs.io/en/latest/dictionary/clone.ini.html>`_


Suggestions
___________

* Only clone containers (like variables, properties...)
* Add typehint to injected properties, so they are checked as objects.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CloneWithNonObject                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.0                                                                                                                                                            |
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


