.. _performances-issetwholearray:

.. _isset()-on-the-whole-array:

Isset() On The Whole Array
++++++++++++++++++++++++++

  `Isset() <https://www.www.php.net/isset>`_ works quietly on a whole array. There is no need to test all previous index before testing for the target index.

It also works on chained properties. 


.. code-block:: php
   
   <?php
   
   // Straight to the point
   if (isset($a[1]['source'])) {
       // Do something with $a[1]['source']
   }
   
   // Doing too much work
   if (isset($a) && isset($a[1]) && isset($a[1]['source'])) {
       // Do something with $a[1]['source']
   }
   
   // Doing too much work
   if (isset($object) && isset($object->p1) && isset($object->p1->property)) {
       // Do something with $object->p1->property
   }
   
   ?>


There is a gain in readability, by avoiding long and hard to read logical expression, and reducing them in one simple `isset() <https://www.www.php.net/isset>`_ call.

There is a gain in performances by using one call to `isset() <https://www.www.php.net/isset>`_, instead of several. It is a micro-optimization.

See also `Isset <http://www.php.net/isset>`_.


Suggestions
___________

* Merge all calls in one, and remove all unnecessary calls to isset()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/IssetWholeArray                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`, :ref:`Suggestions <ruleset-Suggestions>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | coalesce, isset                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tine20-performances-issetwholearray`, :ref:`case-expressionengine-performances-issetwholearray`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


