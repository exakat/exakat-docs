.. _php-newinitializers:

.. _new-initializers:

New Initializers
++++++++++++++++

.. meta::
	:description:
		New Initializers: Parameters, static variables and global constants may be initialized with an object.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: New Initializers
	:twitter:description: New Initializers: Parameters, static variables and global constants may be initialized with an object
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: New Initializers
	:og:type: article
	:og:description: Parameters, static variables and global constants may be initialized with an object
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/NewInitializers.html
	:og:locale: en
Parameters, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables and global constants may be initialized with an object. 
This feature is available in PHP 8.1 and more recent. It is reported as an invalid constant expression in older PHP versions.

.. code-block:: php
   
   <?php
   
   function foo( $a = new A) {
       static $static = new B;
   
   }
   
   const A = new C;
   
   ?>

See also `PHP RFC: New in initializers <https://wiki.php.net/rfc/new_in_initializers>`_ and `Nested Attributes`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Constant+expression+contains+invalid+operations.html>`_



Connex PHP features
-------------------

  + `new-in-initializer <https://php-dictionary.readthedocs.io/en/latest/dictionary/new-in-initializer.ini.html>`_
  + `nested-attribute <https://php-dictionary.readthedocs.io/en/latest/dictionary/nested-attribute.ini.html>`_


Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NewInitializers                                                                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP73 <ruleset-CompatibilityPHP73>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.1                                                                                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                                                                                                                                                                                           |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


