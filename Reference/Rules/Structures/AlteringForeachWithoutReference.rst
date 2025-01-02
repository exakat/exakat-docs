.. _structures-alteringforeachwithoutreference:

.. _altering-foreach-without-reference:

Altering Foreach Without Reference
++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Altering Foreach Without Reference: Foreach() loop that could use a reference as value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Altering Foreach Without Reference
	:twitter:description: Altering Foreach Without Reference: Foreach() loop that could use a reference as value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Altering Foreach Without Reference
	:og:type: article
	:og:description: Foreach() loop that could use a reference as value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Altering Foreach Without Reference.html
	:og:locale: en
`Foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loop that could use a reference as value. 

When using a foreach loop that modifies the original source, it is recommended to use referenced variables, rather than access the original value with $source[$index]. 

Using references is then must faster, and easier to read. 



`array_walk() <https://www.php.net/array_walk>`_ and `array_map() <https://www.php.net/array_map>`_ are also alternative to prevent the use of `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_, when $key is not used.

.. code-block:: php
   
   <?php
   
   // Using references in foreach
   foreach($source as $key => &$value) {
       $value = newValue($value, $key);
   }
   
   // Avoid foreach : use array_map
   $source = array_walk($source, 'newValue');
       // Here, $key MUST be the second argument or newValue
   
   // Slow version to update the array
   foreach($source as $key => &$value) {
       $source[$key] = newValue($value, $key);
   }
   ?>

See also `foreach <https://www.php.net/manual/en/control-structures.foreach.php>`_.

Connex PHP features
-------------------

  + `foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_
  + `loop <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_


Suggestions
___________

* Add the reference on the modified blind variable, and avoid accessing the source array




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/AlteringForeachWithoutReference                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `use-reference-to-alter-in-foreach <https://github.com/dseguy/clearPHP/tree/master/rules/use-reference-to-alter-in-foreach.md>`__                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-contao-structures-alteringforeachwithoutreference`, :ref:`case-wordpress-structures-alteringforeachwithoutreference`                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`dangling-array-references`                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


