.. _constants-unusedconstants:

.. _unused-constants:

Unused Constants
++++++++++++++++

.. meta::
	:description:
		Unused Constants: Those constants are defined in the code but never used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Constants
	:twitter:description: Unused Constants: Those constants are defined in the code but never used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Constants
	:og:type: article
	:og:description: Those constants are defined in the code but never used
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Constants/UnusedConstants.html
	:og:locale: en
Those constants are defined in the code but never used. Defining unused constants slow down the application, as they are executed and stored in PHP hashtables. 
It is recommended to comment them out, and only define them when it is necessary.

.. code-block:: php
   
   <?php
   
   // const-defined constant
   const USED_CONSTANT  = 0;
   const UNUSED_CONSTANT = 1 + USED_CONSTANT;
   
   // define-defined constant
   define('ANOTHER_UNUSED_CONSTANT', 3);
   
   ?>
Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Make use of the constant
* Remove the constant




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/UnusedConstants                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


