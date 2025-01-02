.. _structures-nonullforindex:

.. _no-null-for-index:

No Null For Index
+++++++++++++++++

.. meta::
	:description:
		No Null For Index: Avoid using ``null`` value as an index in an array.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Null For Index
	:twitter:description: No Null For Index: Avoid using ``null`` value as an index in an array
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Null For Index
	:og:type: article
	:og:description: Avoid using ``null`` value as an index in an array
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Null For Index.html
	:og:locale: en
Avoid using ``null`` value as an index in an array. PHP actually casts it to the empty string. This means that later, it might be impossible to find the ``null`` in the list of keys.

.. code-block:: php
   
   <?php
   
   $a = [];
   $a[null] = 1;
   
   print_r(array_keys($a));
   // [''] empty string
   
   ?>
Connex PHP features
-------------------

  + `null <https://php-dictionary.readthedocs.io/en/latest/dictionary/null.ini.html>`_
  + `index-array <https://php-dictionary.readthedocs.io/en/latest/dictionary/index-array.ini.html>`_


Suggestions
___________

* Always checks for null values. Given it then a valid value.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoNullForIndex                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


