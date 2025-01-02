.. _functions-unsetonarguments:

.. _unset-arguments:

Unset Arguments
+++++++++++++++

.. meta::
	:description:
		Unset Arguments: There is no need to unset arguments.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unset Arguments
	:twitter:description: Unset Arguments: There is no need to unset arguments
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unset Arguments
	:og:type: article
	:og:description: There is no need to unset arguments
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unset Arguments.html
	:og:locale: en
There is no need to unset arguments. Those values will be freed at the end of the function anyhow.

.. code-block:: php
   
   <?php
   
   function foo($a, $b) {
       $b = $a * 2;
       // This is useless. $a will be freed at the end of the function.
       unset($a);
   }
   
   ?>
Connex PHP features
-------------------

  + `argument <https://php-dictionary.readthedocs.io/en/latest/dictionary/argument.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UnsetOnArguments                                                                                              |
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


