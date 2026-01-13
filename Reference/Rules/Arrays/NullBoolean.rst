.. _arrays-nullboolean:

.. _null-or-boolean-arrays:

Null Or Boolean Arrays
++++++++++++++++++++++

  Null, int, floats, booleans are valid with PHP array syntx. Yet, they only produces ``null`` values. They also did not emits any warning until PHP 7.4.

Older code used to initialize variables as null, sometimes explictly, and then, use them as arrays. The current support for this syntax is for backward compatibility. 

Illegal keys, such as another array, will also generate a `NULL <https://www.php.net/manual/en/language.types.null.php>`_ value, instead of a Fatal `error <https://www.php.net/error>`_. 


.. code-block:: php
   
   <?php
   
   // outputs NULL
   var_dump(null[0]);
   var_dump(null[[]]);
   
   const MY_CONSTANT = true;
   // outputs NULL
   var_dump(MY_CONSTANT[10]);
   
   ?>

See also `Null and True <https://twitter.com/Chemaclass/status/1144588647464951808>`_.

Related PHP errors 
-------------------

  + `Trying to access array offset on value of type null <https://php-errors.readthedocs.io/en/latest/messages/trying-to-access-array-offset-on-%25s.html>`_
  + `Trying to access array offset on value of type boolean <https://php-errors.readthedocs.io/en/latest/messages/trying-to-access-array-offset-on-%25s.html>`_
  + `Trying to access array offset on value of type float <https://php-errors.readthedocs.io/en/latest/messages/trying-to-access-array-offset-on-%25s.html>`_
  + `Trying to access array offset on value of type int <https://php-errors.readthedocs.io/en/latest/messages/trying-to-access-array-offset-on-%25s.html>`_



Connex PHP features
-------------------

  + `null <https://php-dictionary.readthedocs.io/en/latest/dictionary/null.ini.html>`_
  + `boolean <https://php-dictionary.readthedocs.io/en/latest/dictionary/boolean.ini.html>`_
  + `float <https://php-dictionary.readthedocs.io/en/latest/dictionary/float.ini.html>`_
  + `int <https://php-dictionary.readthedocs.io/en/latest/dictionary/int.ini.html>`_
  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Avoid using the array syntax on null and boolean
* Avoid using null and boolean on constant that are expecting arrays




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/NullBoolean                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.6                                                                                                                   |
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


