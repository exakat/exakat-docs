.. _security-filternotraw:

.. _filter-not-raw:

Filter Not Raw
++++++++++++++

  Report usage of filter functions with the ``FILTER_RAW_UNSAFE`` option. This option is the default one.

.. code-block:: php
   
   <?php
   
   // default to FILTER_RAW_UNSAFE
   filter_var($a);
   
   // explicit no filter
   filter_var($a, FILTER_RAW_UNSAFE);
   
   ?>
Connex PHP features
-------------------

  + `filter <https://php-dictionary.readthedocs.io/en/latest/dictionary/filter.ini.html>`_


Suggestions
___________

* Use a different filter to validate those data.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/FilterNotRaw                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


