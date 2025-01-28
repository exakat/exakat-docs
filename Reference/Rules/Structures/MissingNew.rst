.. _structures-missingnew:

.. _maybe-missing-new:

Maybe Missing New
+++++++++++++++++

.. meta::
	:description:
		Maybe Missing New: This functioncall looks like a class instantiation that is missing the ``new`` keyword.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Maybe Missing New
	:twitter:description: Maybe Missing New: This functioncall looks like a class instantiation that is missing the ``new`` keyword
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Maybe Missing New
	:og:type: article
	:og:description: This functioncall looks like a class instantiation that is missing the ``new`` keyword
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Maybe Missing New.html
	:og:locale: en
This functioncall looks like a class instantiation that is missing the ``new`` keyword.

Any function definition was found for that function, but a class with that name was. New is probably missing.

.. code-block:: php
   
   <?php
   
   // Functioncall
   $a = foo();
   
   // Class definition
   class foo {}
   // Function definition
   function foo {}
   
   
   // Functioncall
   $a = BAR;
   
   // Function definition
   class bar {}
   // Constant definition
   const BAR = 1;
   
   ?>
Connex PHP features
-------------------

  + `new <https://php-dictionary.readthedocs.io/en/latest/dictionary/new.ini.html>`_


Suggestions
___________

* Add the new
* Rename the class to distinguish it from the function
* Rename the function to distinguish it from the class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MissingNew                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


