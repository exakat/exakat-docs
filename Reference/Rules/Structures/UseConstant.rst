.. _structures-useconstant:

.. _use-constant-instead-of-function:

Use Constant Instead Of Function
++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Use Constant Instead Of Function: Some functioncalls have a constant equivalent, that is faster to execute than calling the function.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Constant Instead Of Function
	:twitter:description: Use Constant Instead Of Function: Some functioncalls have a constant equivalent, that is faster to execute than calling the function
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Constant Instead Of Function
	:og:type: article
	:og:description: Some functioncalls have a constant equivalent, that is faster to execute than calling the function
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/UseConstant.html
	:og:locale: en
  Some functioncalls have a constant equivalent, that is faster to execute than calling the function. 

This applies to the following functions : 

* `pi() <https://www.php.net/pi>`_ : replace with `M_PI`
* `phpversion() <https://www.php.net/phpversion>`_ : replace with `PHP_VERSION`
* `php_sapi_name() <https://www.php.net/php_sapi_name>`_ : replace with `PHP_SAPI_NAME`

.. code-block:: php
   
   <?php
   
   // recommended way 
   echo PHP_VERSION;
   
   // slow version
   echo php_version();
   
   ?>

See also `PHP why pi() and M_PI <https://stackoverflow.com/questions/42021176/php-why-pi-and-m-pi>`_.


Suggestions
___________

* Use the constant version, not the function.




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseConstant                                                                                                                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>`, :ref:`php-cs-fixable <ruleset-php-cs-fixable>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


