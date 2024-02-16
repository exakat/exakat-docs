.. _php-avoidgetobjectvars:

.. _avoid-get\_object\_vars():

Avoid get_object_vars()
+++++++++++++++++++++++

  `get_object_vars() <https://www.php.net/get_object_vars>`_ changes behavior between PHP 7.3 and 7.4. It also behaves different within and outside a class. 


.. code-block:: php
   
   <?php
   
   // Illustration courtesy of Doug Bierer
   $obj = new ArrayObject(['A' => 1,'B' => 2,'C' => 3]);
   var_dump($obj->getArrayCopy());
   var_dump(get_object_vars($obj));
   
   ?>

See also `get_object_vars script on 3V4L <https://3v4l.org/ELVGY>`_ and `The Strange Case of ArrayObject <https://phptraining.net/articles/strange_case_of_array_object>`_.


Suggestions
___________

* Use ArrayObject and getArrayCopy() method




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/AvoidGetobjectVars                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.1                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | class, arrayobject                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+


