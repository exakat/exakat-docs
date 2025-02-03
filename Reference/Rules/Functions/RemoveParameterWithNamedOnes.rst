.. _functions-removeparameterwithnamedones:

.. _remove-parameter-with-named-parameters:

Remove Parameter With Named Parameters
++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Remove Parameter With Named Parameters: It is possible to reduce the size of a method call by using named parameter.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Remove Parameter With Named Parameters
	:twitter:description: Remove Parameter With Named Parameters: It is possible to reduce the size of a method call by using named parameter
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Remove Parameter With Named Parameters
	:og:type: article
	:og:description: It is possible to reduce the size of a method call by using named parameter
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Remove Parameter With Named Parameters.html
	:og:locale: en
It is possible to reduce the size of a method call by using named parameter. This is interesting when some of the positional parameter uses their default value. 

Using named parameters allows the code to drop parameter when it is using the default value. This makes the code less bloated, and the parameter names provide a contextual documentation.

On the other hand, removing an explicit argument makes the code depend on the signature. When that signature changes, so does the code behavior.

.. code-block:: php
   
   <?php
   
   function foo($a, $b, $c = null);
   
   // This may have one less parameter, with named parameters
   foo(1,2,null);
   
   // using named parameters
   foo(a:1, b:2);
   
   ?>
Connex PHP features
-------------------

  + `named-parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/named-parameter.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/RemoveParameterWithNamedOnes                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


