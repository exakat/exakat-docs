.. _structures-multipleunset:

.. _multiple-unset():

Multiple Unset()
++++++++++++++++

  Unset() accepts multiple arguments, unsetting them one after each other. It is more efficient to call unset() once, than multiple times.

.. code-block:: php
   
   <?php
   
   // One call to unset only
   unset($a, $b, $c, $d);
   
   // Too many calls to unset
   unset($a);
   unset($b);
   unset($c);
   unset($d);
   
   ?>

See also `unset <https://www.php.net/unset>`_.

Connex PHP features
-------------------

  + `unset <https://php-dictionary.readthedocs.io/en/latest/dictionary/unset.ini.html>`_


Suggestions
___________

* Merge all unset into one call




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MultipleUnset                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`php-cs-fixable <ruleset-php-cs-fixable>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.6                                                                                                                   |
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


