.. _php-usestdclass:

.. _avoid-using-stdclass:

Avoid Using stdClass
++++++++++++++++++++

  ``stdClass`` is the default class for PHP. It is instantiated when PHP needs to return a object, but no class is specifically available.

It is recommended to avoid instantiating this class. Some PHP or frameworks functions, such as `json_encode() <https://www.php.net/json_encode>`_, do return them : this is fine, although it is reported here.

If you need a ``stdClass`` object, it is faster to build it as an array, then cast it, than instantiate ``stdClass``. This is a micro-optimisation.

.. code-block:: php
   
   <?php
   
   $json = '{"a":1,"b":2,"c":3}';
   $object = json_decode($json);
   // $object is a stdClass, as returned by json_decode
   
   // Fast building of $o
   $a = [];
   $a['a'] = 1;
   $a['b'] = 2;
   $a['c'] = 3;
   json_encode( (object) $a);
   
   // Slow building of $o
   $o = new stdClass();
   $o->a = 1;
   $o->b = 2;
   $o->c = 3;
   json_encode($o);
   
   ?>

Suggestions
___________

* Create a custom class to handle the properties




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseStdclass                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | stdclass                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


