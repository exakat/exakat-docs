.. _typehints-couldbefloat:

.. _could-be-float:

Could Be Float
++++++++++++++

.. meta::
	:description:
		Could Be Float: Mark arguments, class constants, properties and return types that can be set to ``float``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Float
	:twitter:description: Could Be Float: Mark arguments, class constants, properties and return types that can be set to ``float``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Float
	:og:type: article
	:og:description: Mark arguments, class constants, properties and return types that can be set to ``float``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Typehints/CouldBeFloat.html
	:og:locale: en
Mark arguments, class constants, properties and return types that can be set to ``float``.

.. code-block:: php
   
   <?php
   
   // Accept an int as input 
   function foo($b) {
       // Returns a float (cubic root of $b);
       return pow($b, 1 / 3);
   }
   
   ?>
Connex PHP features
-------------------

  + `float <https://php-dictionary.readthedocs.io/en/latest/dictionary/float.ini.html>`_


Suggestions
___________

* Add `float` typehint to the code.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeFloat                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Typechecks <ruleset-Typechecks>`                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.4                                                                                                                                                                                   |
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


