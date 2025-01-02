.. _classes-unreachablemethod:

.. _unreachable-method:

Unreachable Method
++++++++++++++++++

.. meta::
	:description:
		Unreachable Method: A method that is never called from the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unreachable Method
	:twitter:description: Unreachable Method: A method that is never called from the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unreachable Method
	:og:type: article
	:og:description: A method that is never called from the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unreachable Method.html
	:og:locale: en
A method that is never called from the code. 

The method has the following characteristics : 
+ not private, aka public or protected
+ The direct class is never instantiated
+ All children classes overwrite this method
+ parent\:\: is never used to reach it

Then, this class is actually dead code.

.. code-block:: php
   
   <?php
   
   class x {
       protected function foox() {}
   }
   
   class xx extends x {
       protected function foox() {}
   }
   ?>
Connex PHP features
-------------------

  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Suggestions
___________

* Make the method abstract and remove the block
* Move the code to one of the child




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnreachableMethod                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Dead code <ruleset-Dead-code>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.6                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


