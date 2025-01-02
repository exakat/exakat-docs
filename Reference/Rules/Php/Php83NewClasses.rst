.. _php-php83newclasses:

.. _php-8.3-new-classes:

Php 8.3 New Classes
+++++++++++++++++++

.. meta::
	:description:
		Php 8.3 New Classes: New classes, introduced in PHP 8.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Php 8.3 New Classes
	:twitter:description: Php 8.3 New Classes: New classes, introduced in PHP 8
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Php 8.3 New Classes
	:og:type: article
	:og:description: New classes, introduced in PHP 8
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Php 8.3 New Classes.html
	:og:locale: en
New classes, introduced in PHP 8.3. If classes where created with the same name, in current code, they have to be moved in a namespace, or removed from code to migrate safely to PHP 8.3.

The new classes are : 

+ ``DateError``
+ ``DateObjectError``
+ ``DateRangeError``
+ ``DateException``
+ ``DateInvalidTimeZoneException``
+ ``DateInvalidOperationException``
+ ``DateMalformedStringException``
+ ``DateMalformedIntervalStringException``
+ ``DateMalformedPeriodStringException``
+ ``Random\`IntervalBoundary <https://www.php.net/intervalboundary>`_``

.. code-block:: php
   
   <?php
   
   namespace {
       // Global namespace
       class DateError {
           // Move to a namespace
           // or, remove this class
       }
   }
   
   namespace B {
       class DateError {
           // This is OK : in a namespace
       }
   }
   
   ?>

See also `New Classes and Interfaces <https://www.php.net/manual/en/migration83.classes.php>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Move the current classes with the same names into a distinct domain name
* Change the name of the class




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php83NewClasses                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP83 <ruleset-CompatibilityPHP83>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.3 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


