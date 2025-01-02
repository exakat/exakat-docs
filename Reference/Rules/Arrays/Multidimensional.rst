.. _arrays-multidimensional:

.. _multidimensional-arrays:

Multidimensional Arrays
+++++++++++++++++++++++

.. meta::
	:description:
		Multidimensional Arrays: Multidimensional arrays are arrays of arrays.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multidimensional Arrays
	:twitter:description: Multidimensional Arrays: Multidimensional arrays are arrays of arrays
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multidimensional Arrays
	:og:type: article
	:og:description: Multidimensional arrays are arrays of arrays
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Multidimensional Arrays.html
	:og:locale: en
Multidimensional arrays are arrays of arrays. Each level of array is called a dimension. The number of dimensions is arbitrary, though it is recommende not to abuse it beyond 4.

.. code-block:: php
   
   <?php
       $x[1][2] = $x[2][3][4];
   ?>

See also `Type array <https://www.php.net/manual/en/language.types.array.php>`_ and `Using Multidimensional Arrays in PHP <https://www.elated.com/articles/php-multidimensional-arrays/>`_.

Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_
  + `multidimensional-array <https://php-dictionary.readthedocs.io/en/latest/dictionary/multidimensional-array.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/Multidimensional                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


