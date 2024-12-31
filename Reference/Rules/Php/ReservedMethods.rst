.. _php-reservedmethods:

.. _reserved-methods:

Reserved Methods
++++++++++++++++

.. meta\:\:
	:description:
		Reserved Methods: PHP has reserved all the methods names, starting with two underscores characters ``__``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Reserved Methods
	:twitter:description: Reserved Methods: PHP has reserved all the methods names, starting with two underscores characters ``__``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Reserved Methods
	:og:type: article
	:og:description: PHP has reserved all the methods names, starting with two underscores characters ``__``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/ReservedMethods.html
	:og:locale: en
  PHP has reserved all the methods names, starting with two underscores characters ``__``. 

While this is not explicitely enforced, using such names may create future conflict if PHP acquire features that rely on them.

.. code-block:: php
   
   <?php
   
   class x {
   	// One of the reserved and used PHP method
   	function __toString() {} 
   
   	// One potential PHP reserved method
   	function __toArray() {} 
   }
   
   ?>

See also `Magic methods <https://www.php.net/manual/en/language.oop5.magic.php>`_.

Connex PHP features
-------------------

  + `naming <https://php-dictionary.readthedocs.io/en/latest/dictionary/naming.ini.html>`_
  + `magic-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Suggestions
___________

* Change the name of the method and avoid prefixing it with ``__``




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ReservedMethods                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.2                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------+


