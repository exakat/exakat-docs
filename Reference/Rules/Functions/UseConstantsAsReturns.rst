.. _functions-useconstantsasreturns:

.. _use-constants-as-returns:

Use Constants As Returns
++++++++++++++++++++++++

.. meta\:\:
	:description:
		Use Constants As Returns: When a native PHP function returns only constants, it is recommended to use those constants to identify the returned values.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Constants As Returns
	:twitter:description: Use Constants As Returns: When a native PHP function returns only constants, it is recommended to use those constants to identify the returned values
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Constants As Returns
	:og:type: article
	:og:description: When a native PHP function returns only constants, it is recommended to use those constants to identify the returned values
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/UseConstantsAsReturns.html
	:og:locale: en
  When a native PHP function returns only constants, it is recommended to use those constants to identify the returned values.

.. code-block:: php
   
   <?php
   
   if (preg_last_error() != PREG_NO_ERROR ) {
       // An error occured with the last Regex call
   }
   
   // Who will guess PREG_JIT_STACKLIMIT_ERROR ? 
   if (preg_last_error() == 6 ) {
       // An error occured with the last Regex call
   }
   
   ?>

Suggestions
___________

* Use the valid constants to identify the results




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UseConstantsAsReturns                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.9                                                                                                                   |
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


