.. _structures-couldcasttoarray:

.. _could-cast-to-array:

Could Cast To Array
+++++++++++++++++++

.. meta::
	:description:
		Could Cast To Array: The array cast operator transform a scalar into an array with that scalar.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Cast To Array
	:twitter:description: Could Cast To Array: The array cast operator transform a scalar into an array with that scalar
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Cast To Array
	:og:type: article
	:og:description: The array cast operator transform a scalar into an array with that scalar
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Cast To Array.html
	:og:locale: en
The array cast operator transform a scalar into an array with that scalar. It also keeps an array as an array, so a single call to ``(array)`` is able to convert scalars to array, while keeping values already in array form intact.

.. code-block:: php
   
   <?php
   
   // 
   if (!is_array($a)) {
   	$a = [$a];
   }
   
   // equivalent to 
   $a = (array) $a;
   
   // same, with the else
   if (is_array($a)) {
   } else {
   	$a = array($a);
   }
   
   ?>

See also `Mastering the (array) Cast Operator in PHP <https://www.exakat.io/en/mastering-the-array-cast-operator-in-php-a-comprehensive-guide/>`_.

Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_
  + `cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_


Suggestions
___________

* Use a direct cast to array




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldCastToArray                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


