.. _extensions-extbcmath:

.. _ext-bcmath:

ext/bcmath
++++++++++

.. meta::
	:description:
		ext/bcmath: Extension BC Math.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/bcmath
	:twitter:description: ext/bcmath: Extension BC Math
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/bcmath
	:og:type: article
	:og:description: Extension BC Math
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/bcmath.html
	:og:locale: en
Extension BC Math.

For arbitrary precision mathematics PHP offers the Binary Calculator which supports numbers of any size and precision up to ``2147483647-1`` (or ``0x7FFFFFFF-1``) decimals, represented as strings.

.. code-block:: php
   
   <?php
   
   echo bcpow('2', '123'); 
   //10633823966279326983230456482242756608
   
   echo 2**123;
   //1.0633823966279E+37
   ?>

See also `BC Math Functions <http://www.php.net/bcmath>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extbcmath                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


