.. _php-compactinexistant:

.. _nonexistent-variable-in-compact():

Nonexistent Variable In compact()
+++++++++++++++++++++++++++++++++

  `Compact() <https://www.php.net/compact>`_ doesn't warn when it tries to work on an nonexistent variable. It just ignores the variable.

This behavior changed in PHP 7.3, and `compact() <https://www.php.net/compact>`_ now emits a warning when the compacted variable doesn't exist.
For performances reasons, this analysis only works inside methods and functions.

.. code-block:: php
   
   <?php
   
   function foo($b = 2) {
       $a = 1;
       // $c doesn't exists, and is not compacted.
       return compact('a', 'b', 'c');
   }
   ?>

See also `compact <http://www.php.net/compact>`_ and `PHP RFC: Make compact function reports undefined passed variables <https://wiki.php.net/rfc/compact>`_.


Suggestions
___________

* Fix the name of variable in the compact() argument list
* Remove the name of variable in the compact() argument list




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CompactInexistant                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP73 <ruleset-CompatibilityPHP73>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.9                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | compact                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


