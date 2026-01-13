.. _php-directcalltoclone:

.. _direct-call-to-\_\_clone():

Direct Call To __clone()
++++++++++++++++++++++++

  Direct call to magic method ``__clone()`` was forbidden. It is allowed since PHP 7.0. 

From the RFC : ``Doing calls like $obj->`__clone( <https://www.php.net/manual/en/language.oop5.magic.php>`_ ) is now allowed. This was the only magic method that had a compile-time check preventing some calls to it, which doesn't make sense. If we allow all other magic methods to be called, there's no reason to forbid this one``.

.. code-block:: php
   
   <?php
   
       class Foo {
           function __clone() {}
       }
       
       $a = new Foo;
       $a->__clone();
   ?>

See also `Directly calling __clone is allowed <https://wiki.php.net/rfc/abstract_syntax_tree#directly_calling_clone_is_allowed>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Cannot+call+__clone%28%29+method+on+objects+-+use+%27clone+%24obj%27+instead.html>`_



Connex PHP features
-------------------

  + `clone <https://php-dictionary.readthedocs.io/en/latest/dictionary/clone.ini.html>`_
  + `magic-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Suggestions
___________

* Use the clone operator to call the __clone magic method




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/DirectCallToClone                                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.8                                                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


