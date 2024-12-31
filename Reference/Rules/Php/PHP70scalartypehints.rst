.. _php-php70scalartypehints:

.. _php-7.0-scalar-typehints:

PHP 7.0 Scalar Typehints
++++++++++++++++++++++++

.. meta\:\:
	:description:
		PHP 7.0 Scalar Typehints: New scalar typehints were introduced : ``bool``, ``int``, ``float``, ``string``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 7.0 Scalar Typehints
	:twitter:description: PHP 7.0 Scalar Typehints: New scalar typehints were introduced : ``bool``, ``int``, ``float``, ``string``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 7.0 Scalar Typehints
	:og:type: article
	:og:description: New scalar typehints were introduced : ``bool``, ``int``, ``float``, ``string``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/PHP70scalartypehints.html
	:og:locale: en
  New scalar typehints were introduced : ``bool``, ``int``, ``float``, ``string``.

They cannot be used before PHP 7.0, and will be confused with classes or interfaces.

.. code-block:: php
   
   <?php
   
   function foo(string $name) {
       print "Hello $name";
   }
   
   foo("Damien"); 
   // display 'Hello Damien'
   
   foo(33); 
   // displays an error
   
   ?>

See also `Scalar type declarations <https://www.php.net/manual/en/migration70.new-features.php#migration70.new-features.scalar-type-declarations>`_ and `PHP 7 SCALAR TYPE DECLARATIONS <https://tutorials.kode-blog.com/php-7-scalar-type-declarations>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/PHP70scalartypehints                                                                                                                                                                                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.5                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


