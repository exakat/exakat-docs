.. _php-usecovariance:

.. _use-covariance:

Use Covariance
++++++++++++++

  Covariance is compatible return typehint. A child class may return an object of a child class of the return type of its `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_'s method.

Since a children class may return a children class of the return type, the evolution is in the same order.

Covariance is a PHP 7.4 feature. Covariance is distinct from argument contravariance.

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

See also `Covariant Returns and Contravariant Parameters <https://wiki.php.net/rfc/covariant-returns-and-contravariant-parameters>`_ and :ref:`No title for `Php/UseContravariance`_ <No anchor for `Php/UseContravariance`_>`.

Connex PHP features
-------------------

  + `covariance <https://php-dictionary.readthedocs.io/en/latest/dictionary/covariance.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseCovariance                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


