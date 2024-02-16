.. _php-php81intersectiontypehint:

.. _intersection-typehint:

Intersection Typehint
+++++++++++++++++++++

  Intersection typehints allows the combination of several typehint for the same argument or return value. 

Several typehints are specified at the same place as a single one. The different values are separated by a ampersand character ``&``. 



Intersection types are a PHP 8.1 new feature.

.. code-block:: php
   
   <?php
   
   class Number {
       private A&B $object;
   }
   ?>

See also `PHP RFC: Pure intersection types <https://wiki.php.net/rfc/pure-intersection-types>`_, `Type declarations <https://www.php.net/manual/en/language.types.declarations.php>`_ and `How the New Intersection Types in PHP 8.1 Give You More Flexibility <https://www.cloudsavvyit.com/12907/how-the-new-intersection-types-in-php-8-1-give-you-more-flexibility/>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php81IntersectionTypehint                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | typehint, union-type                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


