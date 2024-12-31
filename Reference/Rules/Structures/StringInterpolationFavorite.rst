.. _structures-stringinterpolationfavorite:

.. _string-interpolation-favorite:

String Interpolation Favorite
+++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		String Interpolation Favorite: This analysis collects the various ways that string interpolation is done inside strings.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: String Interpolation Favorite
	:twitter:description: String Interpolation Favorite: This analysis collects the various ways that string interpolation is done inside strings
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: String Interpolation Favorite
	:og:type: article
	:og:description: This analysis collects the various ways that string interpolation is done inside strings
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/StringInterpolationFavorite.html
	:og:locale: en
  This analysis collects the various ways that string interpolation is done inside strings. Until PHP 8.1, there were 4 ways :

.. code-block:: php
   
   <?php
   
   $a = "$variable";
   $a = "$object->property";
   $a = "$array[index]";
   
   $a = "";
   $a = "{$variable}";
   
   $a = "";
   ?>
Connex PHP features
-------------------

  + `interpolation <https://php-dictionary.readthedocs.io/en/latest/dictionary/interpolation.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/StringInterpolationFavorite                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


