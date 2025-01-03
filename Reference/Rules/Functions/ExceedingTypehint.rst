.. _functions-exceedingtypehint:

.. _exceeding-typehint:

Exceeding Typehint
++++++++++++++++++

.. meta::
	:description:
		Exceeding Typehint: The typehint is not fully used in the method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Exceeding Typehint
	:twitter:description: Exceeding Typehint: The typehint is not fully used in the method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Exceeding Typehint
	:og:type: article
	:og:description: The typehint is not fully used in the method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Exceeding Typehint.html
	:og:locale: en
The typehint is not fully used in the method. Some of the defined methods in the typehint are unused. A tighter typehint could be used, to avoid method pollution.
Tight typehint prevents the argument from doing too much. They also require more maintenance : creation of dedicated interfaces, method management to keep all typehint tight.

.. code-block:: php
   
   <?php
   
   interface i {
       function i1();
       function i2();
   }
   
   interface j {
       function j1();
       function j2();
   }
   
   function foo(i $a, j $b) {
       // the i typehint is totally used
       $a->i1();
       $a->i2();
       
       // the i typehint is not totally used : j2() is not used.
       $b->j1();
   }
   
   ?>

See also :ref:`Insufficient Typehint <insufficient-typehint>`.

Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Suggestions
___________

* Keep the typehint tight, do not inject more than needed.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/ExceedingTypehint                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.3                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


