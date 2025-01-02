.. _functions-couldtypewitharray:

.. _could-type-with-array:

Could Type With Array
+++++++++++++++++++++

.. meta::
	:description:
		Could Type With Array: That argument may be typed with ``array``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Type With Array
	:twitter:description: Could Type With Array: That argument may be typed with ``array``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Type With Array
	:og:type: article
	:og:description: That argument may be typed with ``array``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Type With Array.html
	:og:locale: en
That argument may be typed with ``array``. Based on usage, it was determined that the only type possible is a array.

.. code-block:: php
   
   <?php
   
   // $a is used with a function which requires an int. 
   function foo($a) {
       return array_keys($a);
   }
   
   ?>

See also `Type declarations <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Add the ``array`` typehint to the function.
* Add the ``iterable`` typehint to the function.
* Add the ``traversable`` typehint to the function.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/CouldTypeWithArray                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


