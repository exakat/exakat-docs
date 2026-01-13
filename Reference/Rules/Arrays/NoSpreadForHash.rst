.. _arrays-nospreadforhash:

.. _no-spread-for-hash:

No Spread For Hash
++++++++++++++++++

  The spread operator ``...`` used to work only on integer-indexed arrays. This limitation was removed in PHP 8.1 and more recent.

.. code-block:: php
   
   <?php
   
   // This is valid, as ``"-33"`` is cast to integer by PHP automagically
   var_dump(...[1,"-33" => 2, 3]);
   
   // This is not valid
   var_dump(...[1,"C" => 2, 3]);
   
   ?>

See also `Variable-length argument lists <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_.

Related PHP errors 
-------------------

  + `Cannot unpack array with string keys <https://php-errors.readthedocs.io/en/latest/messages/cannot-unpack-array-with-string-keys.html>`_
  + `array_merge() does not accept unknown named parameters <https://php-errors.readthedocs.io/en/latest/messages/array_merge%28%29-does-not-accept-unknown-named-parameters.html>`_



Connex PHP features
-------------------

  + `ellipsis <https://php-dictionary.readthedocs.io/en/latest/dictionary/ellipsis.ini.html>`_
  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_
  + `array-spread <https://php-dictionary.readthedocs.io/en/latest/dictionary/array-spread.ini.html>`_


Suggestions
___________

* Add a call to array_values() instead of the hash
* Check the arguments beforehand with array_is_list()
* Upgrade to PHP 8.1




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/NoSpreadForHash                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


