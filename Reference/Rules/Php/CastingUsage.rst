.. _php-castingusage:

.. _cast-usage:

Cast Usage
++++++++++

.. meta::
	:description:
		Cast Usage: List of all cast usage.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Cast Usage
	:twitter:description: Cast Usage: List of all cast usage
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Cast Usage
	:og:type: article
	:og:description: List of all cast usage
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Cast Usage.html
	:og:locale: en
List of all cast usage.

PHP does not require (or support) explicit type definition in variable declaration; a variable's type is determined by the context in which the variable is used. 
Until PHP 7.2, a ``(unset)`` operator was available. It had the same role as ``unset()`` as a function.

.. code-block:: php
   
   <?php
   
   if (is_int($_GET['x'])) {
       $number = (int) $_GET['x'];
   } else {
       error_display('a wrong value was provided for "x"');
   }
   
   ?>

See also `Type Juggling <https://www.php.net/manual/en/language.types.type-juggling.php>`_ and `unset <https://www.php.net/unset>`_.

Connex PHP features
-------------------

  + `cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CastingUsage                                                                                                                                                                        |
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


