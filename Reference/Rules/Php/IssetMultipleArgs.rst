.. _php-issetmultipleargs:

.. _isset-multiple-arguments:

Isset Multiple Arguments
++++++++++++++++++++++++

  `isset() <https://www.www.php.net/isset>`_ may be used with multiple arguments and acts as a AND.

.. code-block:: php
   
   <?php
   
   // isset without and 
   if (isset($a, $b, $c)) {
       // doSomething()
   }
   
   // isset with and 
   if (isset($a) && isset($b) && isset($c)) {
       // doSomething()
   }
   
   ?>

See also `Isset <http://www.php.net/isset>`_.

Connex PHP features
-------------------

  + `isset <https://php-dictionary.readthedocs.io/en/latest/dictionary/isset.ini.html>`_
  + `coalesce <https://php-dictionary.readthedocs.io/en/latest/dictionary/coalesce.ini.html>`_


Suggestions
___________

* Merge all isset() calls into one




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/IssetMultipleArgs                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`php-cs-fixable <ruleset-php-cs-fixable>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.4                                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-thinkphp-php-issetmultipleargs`, :ref:`case-livezilla-php-issetmultipleargs`                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


