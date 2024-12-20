.. _php-usednf:

.. _use-dnf:

Use DNF
+++++++

  This rule detects the usage of the DNF. DNF is the disjunctive Normal Form. It is a syntax to handle union and intersectional types at the same time. It was introducted in PHP 8.2.

DNF is available for every typed element of PHP : properties, arguments and returntype. It was extended to class constants on PHP 8.3. 

.. code-block:: php
   
   <?php
   
   class x {
   	const (A&B)|string C = 'string';
   
   	function foo((A&B)|(C&D) $e) {}
   
   }
   
   ?>

See also `PHP 8.2: DNF Types <https://php.watch/versions/8.2/dnf-types>`_.

Connex PHP features
-------------------

  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_
  + `dnf-type <https://php-dictionary.readthedocs.io/en/latest/dictionary/dnf-type.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseDNF                                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.2 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


