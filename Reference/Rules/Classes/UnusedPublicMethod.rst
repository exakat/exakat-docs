.. _classes-unusedpublicmethod:

.. _unused-public-methods:

Unused Public Methods
+++++++++++++++++++++

  This rule lists unused public methods. 

Unused public methods are declared as ``public`` in the class, but never called, including outside the class.

.. code-block:: php
   
   <?php
   
   class x {
   	public function usedMethod() {}
   	
   	// There is no call to this method
   	public function unusedMethod() {}
   }
   
   $x = new x();
   $x->usedMethod();
   
   
   ?>
Connex PHP features
-------------------

  + `public <https://php-dictionary.readthedocs.io/en/latest/dictionary/public.ini.html>`_
  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnusedPublicMethod                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`unused-private-methods`, :ref:`unused-protected-methods`, :ref:`unused-methods`                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


