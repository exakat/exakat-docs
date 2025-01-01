.. _functions-adddefaultvalue:

.. _add-default-value:

Add Default Value
+++++++++++++++++

.. meta::
	:description:
		Add Default Value: Parameter in methods definition may receive a default value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Add Default Value
	:twitter:description: Add Default Value: Parameter in methods definition may receive a default value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Add Default Value
	:og:type: article
	:og:description: Parameter in methods definition may receive a default value
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/AddDefaultValue.html
	:og:locale: en
Parameter in methods definition may receive a default value. This allows the called method to set a value when the parameter is omitted.

.. code-block:: php
   
   <?php
   
   function foo($i) {
       if (!is_integer($i)) {
           $i = 0;
       }
   }
   
   ?>

See also `Function arguments <https://www.php.net/manual/en/functions.arguments.php>`_.

Connex PHP features
-------------------

  + `default-value <https://php-dictionary.readthedocs.io/en/latest/dictionary/default-value.ini.html>`_


Suggestions
___________

* Add a default value for parameters




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/AddDefaultValue                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-functions-adddefaultvalue`, :ref:`case-typo3-functions-adddefaultvalue`                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


