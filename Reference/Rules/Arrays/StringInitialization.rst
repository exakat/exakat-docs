.. _arrays-stringinitialization:

.. _array-with-string-initialization:

Array With String Initialization
++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Array With String Initialization: It used to be possible to initialize a variable with an string, and use it as an array.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Array With String Initialization
	:twitter:description: Array With String Initialization: It used to be possible to initialize a variable with an string, and use it as an array
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Array With String Initialization
	:og:type: article
	:og:description: It used to be possible to initialize a variable with an string, and use it as an array
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Arrays/StringInitialization.html
	:og:locale: en
  It used to be possible to initialize a variable with an string, and use it as an array. It is not the case anymore in PHP 7.1.

.. code-block:: php
   
   <?php
   
   // Initialize arrays with array()
   $a = array();
   $a[3] = "4";
   
   // Don't start with a string
   $a = '';
   $a[3] = "4";
   print $a;
   
   // Don't start with a string
   if (is_numeric($a)) {
       $a[] = $a;
   }
   
   ?>

See also `PHP 7.1 no longer converts string to arrays the first time a value is assigned with square bracket notation <https://www.drupal.org/project/adaptivetheme/issues/2832900>`_.

Related PHP errors 
-------------------

  + `Cannot use a scalar value as an array <https://php-errors.readthedocs.io/en/latest/messages/cannot-use-a-scalar-value-as-an-array.html>`_



Connex PHP features
-------------------

  + `initialisation <https://php-dictionary.readthedocs.io/en/latest/dictionary/initialisation.ini.html>`_


Suggestions
___________

* Always initialize arrays with an empty array(), not a string.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/StringInitialization                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.5                                                                                                                   |
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


