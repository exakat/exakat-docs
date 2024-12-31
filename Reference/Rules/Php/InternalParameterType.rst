.. _php-internalparametertype:

.. _wrong-parameter-type:

Wrong Parameter Type
++++++++++++++++++++

.. meta\:\:
	:description:
		Wrong Parameter Type: The expected parameter is not of the correct type.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong Parameter Type
	:twitter:description: Wrong Parameter Type: The expected parameter is not of the correct type
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong Parameter Type
	:og:type: article
	:og:description: The expected parameter is not of the correct type
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/InternalParameterType.html
	:og:locale: en
  The expected parameter is not of the correct type. Check PHP documentation to know which is the right format to be used.

.. code-block:: php
   
   <?php
   
   // substr() shouldn't work on integers.
   // the first argument is first converted to string, and it is 123456.
   echo substr(123456, 0, 4); // display 1234
   
   // substr() shouldn't work on boolean
   // the first argument is first converted to string, and it is 1, and not t
   echo substr(true, 0, 1); // displays 1
   
   // substr() works correctly on strings.
   echo substr(123456, 0, 4);
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Argument+must+be+of+type+int%2C+array+given.html>`_




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/InternalParameterType                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zencart-php-internalparametertype`                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


