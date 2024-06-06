.. _php-usecontravariance:

.. _use-contravariance:

Use Contravariance
++++++++++++++++++

  Contravariance is compatible argument typehint. A child class may accept an object of a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class of the argument type of its `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_'s method.

Since a children class may accept a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class of the argument type, the evolution is in opposite order. 

Contravariance is a PHP 7.4 feature. Contravariance is distinct from return type covariance.

.. code-block:: php
   
   <?php
   class X {
     function m(Y $z): X {}
   }
   
   // m is overwriting the parent's method. 
   // The return type is different.
   // The return type is compatible, as Y is also a sub-class of X.
   class Y extends X {
     function m(X $z): Y {}
   }
   
   ?>

See also `Covariant Returns and Contravariant Parameters <https://wiki.php.net/rfc/covariant-returns-and-contravariant-parameters>`_ and :ref:`No title for `Php/UseCovariance` <No anchor for `Php/UseCovariance`>`.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseContravariance                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | type-covariance, type-contravariance                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


