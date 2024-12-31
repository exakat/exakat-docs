.. _functions-usedfunctions:

.. _used-functions:

Used Functions
++++++++++++++

.. meta\:\:
	:description:
		Used Functions: The functions below are used in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Used Functions
	:twitter:description: Used Functions: The functions below are used in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Used Functions
	:og:type: article
	:og:description: The functions below are used in the code
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/UsedFunctions.html
	:og:locale: en
  The functions below are used in the code.

A function is used in the code when it is called literally, or as a string callback.

.. code-block:: php
   
   <?php
   
   function used() {}
   // The 'unused' function is defined but never called
   function unused() {}
   
   // The 'used' function is called at least once
   used();
   
   // The 'used' function is called as a callback
   array_filter($array, 'used');
   
   ?>
Connex PHP features
-------------------

  + `function <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `unused <https://php-dictionary.readthedocs.io/en/latest/dictionary/unused.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UsedFunctions                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


