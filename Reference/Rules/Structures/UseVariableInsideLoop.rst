.. _structures-usevariableinsideloop:

.. _use-variable-created-inside-loop:

Use Variable Created Inside Loop
++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Use Variable Created Inside Loop: When a variable is created inside a loop, it should also be used in the loop.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Variable Created Inside Loop
	:twitter:description: Use Variable Created Inside Loop: When a variable is created inside a loop, it should also be used in the loop
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Variable Created Inside Loop
	:og:type: article
	:og:description: When a variable is created inside a loop, it should also be used in the loop
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use Variable Created Inside Loop.html
	:og:locale: en
When a variable is created inside a loop, it should also be used in the loop. Otherwise, the variable will be overwritten by each loop, and become dead code.

.. code-block:: php
   
   <?php
   
   foreach($a as $b => $c) {
       $c = 1; 
   }
   
   ?>
Connex PHP features
-------------------

  + `loop <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_


Suggestions
___________

* Remove the variable from the loop
* Add usage to that variable inside the loop
* Turn the variable into a property




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseVariableInsideLoop                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.7                                                                                                                   |
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


