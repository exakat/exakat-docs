.. _attributes-nonamedarguments:

.. _no-named-parameters:

No Named Parameters
+++++++++++++++++++

.. meta::
	:description:
		No Named Parameters: Named parameters were introduced in PHP 8.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Named Parameters
	:twitter:description: No Named Parameters: Named parameters were introduced in PHP 8
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Named Parameters
	:og:type: article
	:og:description: Named parameters were introduced in PHP 8
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Attributes/NoNamedArguments.html
	:og:locale: en
Named parameters were introduced in PHP 8.0. They introduce a strong coupling between the parameter names and the calling structure: changing the parameter name breaks the call. 

To avoid this, case by base, PHP.watch introduced the ``no-named-parameters`` PHP doc commend, which allows method owners to signal that the calls should not use the named parameters. 

This analysis explicit named parameters. Named parameters in arrays are still to do.


.. code-block:: php
   
   <?php
   
   /**
     * no-named-parameters
     */
   function goo($a) {}
   goo(a:1); // This is forbidden
   
   ?>
Connex PHP features
-------------------

  + `named-parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/named-parameter.ini.html>`_


Suggestions
___________

* Remove the name of the parameter; check the order of the parameters.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Attributes/NoNamedArguments                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Attributes <ruleset-Attributes>`                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


