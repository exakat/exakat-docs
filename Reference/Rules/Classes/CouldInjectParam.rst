.. _classes-couldinjectparam:

.. _could-inject-parameter:

Could Inject Parameter
++++++++++++++++++++++

  The parameter is immediately used to create an object. It could be interesting to replace it with an injection of that object's type to keep the method generic.

.. code-block:: php
   
   <?php
   
   class x {
   
   	// The directory is immediately injected 
   	function foo(Directory $dir) {
   		$this->dir = $dir;
   	}
   
   	// Path is injected, then turned into a directory
   	function bar(string $path) {
   		$this->dir = new Directory($path);
   	}
   }
   ?>
Connex PHP features
-------------------

  + `injection <https://php-dictionary.readthedocs.io/en/latest/dictionary/injection.ini.html>`_
  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Suggestions
___________

* Use the instantiation as the type of the parameter.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldInjectParam                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.7                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


