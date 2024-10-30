.. _arrays-slicefirst:

.. _slice-arrays-first:

Slice Arrays First
++++++++++++++++++

  Always start by reducing an array before applying some transformation on it. The shorter array will be processed faster. 



The gain produced here is greater with longer arrays, or greater reductions. They may also be used in loops. This is a micro-optimisation when used on short arrays.

.. code-block:: php
   
   <?php
   
   // fast version
   $a = array_map('foo', array_slice($array, 2, 5));
   
   // slower version
   $a = array_slice(array_map('foo', $array), 2, 5);
   ?>
Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Use the array transforming function on the result of the array shortening function.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/SliceFirst                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`, :ref:`Suggestions <ruleset-Suggestions>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-arrays-slicefirst`                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


