.. _typehints-couldbestring:

.. _could-be-string:

Could Be String
+++++++++++++++

.. meta::
	:description:
		Could Be String: Mark arguments, properties, constants and return types that can be set to ``string``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be String
	:twitter:description: Could Be String: Mark arguments, properties, constants and return types that can be set to ``string``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be String
	:og:type: article
	:og:description: Mark arguments, properties, constants and return types that can be set to ``string``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Typehints/CouldBeString.html
	:og:locale: en
Mark arguments, properties, constants and return types that can be set to ``string``.

.. code-block:: php
   
   <?php
   
   // Accept a string as input 
   function foo($a) {
       // Returns a string
       return $a . 'string';
   }
   
   ?>
Connex PHP features
-------------------

  + `string <https://php-dictionary.readthedocs.io/en/latest/dictionary/string.ini.html>`_


Suggestions
___________

* Choose the string typehint, and add it to the code.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeString                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Typechecks <ruleset-Typechecks>`                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


