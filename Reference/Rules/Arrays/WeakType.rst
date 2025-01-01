.. _arrays-weaktype:

.. _weak-type-with-array:

Weak Type With Array
++++++++++++++++++++

.. meta::
	:description:
		Weak Type With Array: Using array as a type, to use specific index later.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Weak Type With Array
	:twitter:description: Weak Type With Array: Using array as a type, to use specific index later
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Weak Type With Array
	:og:type: article
	:og:description: Using array as a type, to use specific index later
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Arrays/WeakType.html
	:og:locale: en
Using array as a type, to use specific index later.

The type of array is too weak : it allows to know that the array syntax has to be used in the function. Yet, it doesn't enforce the presence or absence of a specific index.

.. code-block:: php
   
   <?php
   
   function foo(array $variable) {
   	echo $array['display'];
   }
   
   ?>

See also `Stop using Arrays <https://jeanhertel.com.br/en/stop-using-arrays>`_ and `Never* Use Arrays <https://presentations.garfieldtech.com/slides-never-use-arrays/phpugffm2020/#/>`_.

Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Use a class as type, instead of 




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/WeakType                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.1                                                                                                                   |
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


