.. _typehints-standalonetypetfn:

.. _standalonetype-true-false-null:

StandaloneType True False Null
++++++++++++++++++++++++++++++

  Report usage of standalone types of true, false and null. 

false and null were added to PHP in PHP 8.2, as standalone types : they can be used alone in a type declaration (property, argument or returntype). true was added in PHP 8.3.

.. code-block:: php
   
   <?php
   
   // simplistic example
   function foo(true $t) : false {
   	return false;
   }
   
   ?>

See also `What's the 'true' Standalone Type in PHP? <https://www.designcise.com/web/tutorial/what-is-the-true-standalone-type-in-php>`_.

Connex PHP features
-------------------

  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/StandaloneTypeTFN                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


