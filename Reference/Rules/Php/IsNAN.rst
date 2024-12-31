.. _php-isnan:

.. _manipulates-nan:

Manipulates NaN
+++++++++++++++

.. meta\:\:
	:description:
		Manipulates NaN: This code handles ``Not-a-Number`` situations.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Manipulates NaN
	:twitter:description: Manipulates NaN: This code handles ``Not-a-Number`` situations
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Manipulates NaN
	:og:type: article
	:og:description: This code handles ``Not-a-Number`` situations
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/IsNAN.html
	:og:locale: en
  This code handles ``Not-a-Number`` situations. ``Not-a-Number``, also called ``NaN``, happens when a calculation can't return an actual float.

.. code-block:: php
   
   <?php
   
   // acos returns a float, unless it is not possible.
   $a = acos(8);
   
   var_dump(is_nan($a));
   
   ?>

See also `Floats <https://www.php.net/manual/en/language.types.float.php>`_.

Connex PHP features
-------------------

  + `float <https://php-dictionary.readthedocs.io/en/latest/dictionary/float.ini.html>`_


Suggestions
___________

* Add the third argument, and set it to true




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/IsNAN                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.6                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


