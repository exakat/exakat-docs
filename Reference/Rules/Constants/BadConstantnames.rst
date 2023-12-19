.. _constants-badconstantnames:

.. _bad-constants-names:

Bad Constants Names
+++++++++++++++++++

  PHP's manual recommends that developer do not use constants with the convention ``__NAME__``. Those are reserved for PHP future use. 

For example, ``__TRAIT__`` recently appeared in PHP, as a magic constant. In the future, other may appear. 


.. code-block:: php
   
   <?php
   
   const __MY_APP_CONST__ = 1;
   
   const __MY_APP_CONST__ = 1;
   
   define('__MY_OTHER_APP_CONST__', 2);
   
   ?>


The analyzer will report any constant which name is ``__.*.__``, or even ``_.*_`` (only one underscore).

See also `Constants <https://www.php.net/manual/en/language.constants.php>`_.


Suggestions
___________

* Avoid using names that doesn't comply with PHP's convention




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/BadConstantnames                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | constant                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-prestashop-constants-badconstantnames`, :ref:`case-zencart-constants-badconstantnames`                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


