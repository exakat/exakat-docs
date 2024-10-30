.. _type-duplicateliteral:

.. _duplicate-literal:

Duplicate Literal
+++++++++++++++++

  Report literals that are repeated across the code. The minimum replication is 5, and is configurable with ``maxDuplicate``.

Repeated literals should be considered a prime candidate for constants.

Integer, reals and strings are considered here. Boolean, Null and Arrays are omitted. 0, 1, 2, 10 and the empty string are all omitted, as too common. This list of omitted constants may be configured with the ``ignoreList`` parameter : a comma separated list of values.

.. code-block:: php
   
   <?php
       // array index are omitted
       $x[3] = 'b';
   
       // constanst are omitted
       const X = 11;
       define('Y', 'string')
   
       // 0, 1, 2, 10 are omitted
       $x = 0; 
       
   ?>

+--------------+----------+---------+---------------------------------------------------------------+
| Name         | Default  | Type    | Description                                                   |
+--------------+----------+---------+---------------------------------------------------------------+
| minDuplicate | 15       | integer | Minimal number of duplication before the literal is reported. |
+--------------+----------+---------+---------------------------------------------------------------+
| ignoreList   | 0,1,2,10 | array   | Common values that have to be ignored. Comma separated list.  |
+--------------+----------+---------+---------------------------------------------------------------+


Connex PHP features
-------------------

  + `literal <https://php-dictionary.readthedocs.io/en/latest/dictionary/literal.ini.html>`_


Suggestions
___________

* Create a constant and use it in place of the literal
* Create a class constant and use it in place of the literal




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/DuplicateLiteral                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


