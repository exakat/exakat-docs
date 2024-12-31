.. _functions-couldtypewithbool:

.. _could-type-with-boolean:

Could Type With Boolean
+++++++++++++++++++++++

.. meta\:\:
	:description:
		Could Type With Boolean: That argument, property or method may be typed with ``bool``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Type With Boolean
	:twitter:description: Could Type With Boolean: That argument, property or method may be typed with ``bool``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Type With Boolean
	:og:type: article
	:og:description: That argument, property or method may be typed with ``bool``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/CouldTypeWithBool.html
	:og:locale: en
  That argument, property or method may be typed with ``bool``. Based on usage, it was determined that the only type possible is a boolean.

.. code-block:: php
   
   <?php
   
   // $a is used with a function which requires a boolean. 
   function foo($code, $a) {
       return var_dump($code, $a);
   }
   
   ?>

See also `Type declarations <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_.

Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Suggestions
___________

* Add the ``bool`` typehint to the function.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/CouldTypeWithBool                                                                                             |
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


