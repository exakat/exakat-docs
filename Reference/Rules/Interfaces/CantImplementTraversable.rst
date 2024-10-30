.. _interfaces-cantimplementtraversable:

.. _can't-implement-traversable:

Can't Implement Traversable
+++++++++++++++++++++++++++

  It is not possible to implement the ``Traversable`` interface. The alternative is to implement ``Iterator`` or ``IteratorAggregate``, which also implements ``Traversable``.

``Traversable`` may be useful when used with ``instanceof``.

.. code-block:: php
   
   <?php
   
   // This lints, but doesn't run
   class x implements Traversable {
   
   }
   
   if( $argument instanceof Traversable ) {
       // doSomething
   }
   
   ?>

See also `Traversable <https://www.php.net/manual/en/class.traversable.php>`_, `Iterator <https://www.php.net/manual/en/class.iterator.php>`_ and `IteratorAggregate <https://www.php.net/manual/en/class.iteratoraggregate.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Class+x+must+implement+interface+Traversable+as+part+of+either+Iterator+or+IteratorAggregate.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/Class+b+cannot+implement+previously+implemented+interface+i.html>`_



Connex PHP features
-------------------

  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Suggestions
___________

* Implement Iterator or IteratorAggregate




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/CantImplementTraversable                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.8                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


