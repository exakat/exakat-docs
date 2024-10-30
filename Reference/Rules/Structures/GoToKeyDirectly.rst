.. _structures-gotokeydirectly:

.. _find-key-directly:

Find Key Directly
+++++++++++++++++

  There is no need to use `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ to search for a key. 

PHP offers two solutions : `array_search() <https://www.php.net/array_search>`_ and `array_keys() <https://www.php.net/array_keys>`_. `Array_search() <https://www.php.net/array_search>`_ finds the first key that fits a value, and `array_keys() <https://www.php.net/array_keys>`_ returns all the keys.

.. code-block:: php
   
   <?php
   
   $array = ['a', 'b', 'c', 'd', 'e'];
   
   print array_search($array, 'c'); 
   // print 2 => 'c';
   
   print_r(array_keys($array, 'c')); 
   // print 2 => 'c';
   
   ?>

See also `array_search <https://www.php.net/array_search>`_ and `array_keys <https://www.php.net/array_keys>`_.

Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Suggestions
___________

* Use array_search()
* Use array_keys()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/GoToKeyDirectly                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


