.. _dump-constantorder:

.. _constant-order:

Constant Order
++++++++++++++

.. meta::
	:description:
		Constant Order: Order of dependency of constants.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Constant Order
	:twitter:description: Constant Order: Order of dependency of constants
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Constant Order
	:og:type: article
	:og:description: Order of dependency of constants
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Dump/ConstantOrder.html
	:og:locale: en
Order of dependency of constants. 

Constants, either global or class, may be built using `static <https://www.php.net/manual/en/language.oop5.static.php>`_ expression. In turn, this means that constants have now a build order. For example : 
The code above leads to the following order : ``A`` - ``B``, ``C``. ``A`` can be built without constraints, while ``B`` and ``C`` must be build when ``A`` is available. Note that ``B`` and ``C`` are both dependant on ``A``, but are not dependant on each other.

The resulting tree displays the different relationship between the constants. 

Note : ``define``constants are not considered here. Only ``const`` constants, global or class.

.. code-block:: php
   
   <?php
   
   // A is an independant global constant
   const A = 1;
   // B is an dependant global constant : it is built with A
   const B = A + 1;
   
   class x {
       // x::C is an dependant class constant : it is built with A 
       const C = A + 3;
   }
   
   ?>

Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/ConstantOrder                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.7                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


