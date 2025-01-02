.. _structures-cancountnoncountable:

.. _can't-count-non-countable:

Can't Count Non-Countable
+++++++++++++++++++++++++

.. meta::
	:description:
		Can't Count Non-Countable: Count() emits an error when it tries to count scalars or objects what don't implement Countable interface.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Can't Count Non-Countable
	:twitter:description: Can't Count Non-Countable: Count() emits an error when it tries to count scalars or objects what don't implement Countable interface
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Can't Count Non-Countable
	:og:type: article
	:og:description: Count() emits an error when it tries to count scalars or objects what don't implement Countable interface
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Can't Count Non-Countable.html
	:og:locale: en
`Count() <https://www.php.net/count>`_ emits an `error <https://www.php.net/error>`_ when it tries to count scalars or objects what don't implement `Countable <https://www.php.net/countable>`_ interface.

.. code-block:: php
   
   <?php
   
   // Normal usage
   $a = array(1,2,3,4);
   echo count($a)." items\n";
   
   // Error emiting usage
   $a = '1234';
   echo count($a)." chars\n";
   
   // Error emiting usage
   echo count($unsetVar)." elements\n";
   
   ?>

See also `Warn when counting non-countable types <https://www.php.net/manual/en/migration72.incompatible.php#migration72.incompatible.warn-on-non-countable-types>`_.

Connex PHP features
-------------------

  + `countable <https://php-dictionary.readthedocs.io/en/latest/dictionary/countable.ini.html>`_


Suggestions
___________

* Add a check before using count such as a type check 




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CanCountNonCountable                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


