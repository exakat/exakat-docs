.. _functions-couldtypewithstring:

.. _could-type-with-string:

Could Type With String
++++++++++++++++++++++

.. meta::
	:description:
		Could Type With String: That argument may be typed with ``string``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Type With String
	:twitter:description: Could Type With String: That argument may be typed with ``string``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Type With String
	:og:type: article
	:og:description: That argument may be typed with ``string``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Type With String.html
	:og:locale: en
That argument may be typed with ``string``.

.. code-block:: php
   
   <?php
   
   // $a is used with a function which requires a string. 
   function foo($a) {
       return strtolower($a);
   }
   
   ?>

See also `Type declarations <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_.

Connex PHP features
-------------------

  + `string <https://php-dictionary.readthedocs.io/en/latest/dictionary/string.ini.html>`_


Suggestions
___________

* Add the ``string`` typehint to the function.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/CouldTypeWithString                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
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


