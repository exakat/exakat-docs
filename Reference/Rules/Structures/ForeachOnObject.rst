.. _structures-foreachonobject:

.. _foreach()-on-object:

foreach() On Object
+++++++++++++++++++

.. meta::
	:description:
		foreach() On Object: This analysis reports usage of a foreach() structure on an object.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: foreach() On Object
	:twitter:description: foreach() On Object: This analysis reports usage of a foreach() structure on an object
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: foreach() On Object
	:og:type: article
	:og:description: This analysis reports usage of a foreach() structure on an object
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/foreach() On Object.html
	:og:locale: en
This analysis reports usage of a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ structure on an object. That object shall not be an array, nor an object with array syntax, such as ``Traversable``.

.. code-block:: php
   
   <?php
   
   $a = new Stdclass();
   $a->p = 1;
   $a->q = 2;
   
   foreach($object as $property => $value) {
       print $property . ' => '. $value.PHP_EOL;
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ForeachOnObject                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                   |
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


