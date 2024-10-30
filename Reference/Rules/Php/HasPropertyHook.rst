.. _php-haspropertyhook:

.. _has-property-hook:

Has Property Hook
+++++++++++++++++

  The analyzed code makes use of property hook. They were introduced in PHP 8.4.

.. code-block:: php
   
   <?php
   
   class x {
   	private string $p {
   		get => $this->p;
   		
   		set { $this-> = mb_strtolower($p);}
   	}
   }
   
   ?>
Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------+
| Short name   | Php/HasPropertyHook                                        |
+--------------+------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>` |
+--------------+------------------------------------------------------------+
| Exakat since | 2.6.8                                                      |
+--------------+------------------------------------------------------------+
| PHP Version  | With PHP 8.4 and more recent                               |
+--------------+------------------------------------------------------------+
| Severity     | Minor                                                      |
+--------------+------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                            |
+--------------+------------------------------------------------------------+
| Precision    | Very high                                                  |
+--------------+------------------------------------------------------------+
| Available in |                                                            |
+--------------+------------------------------------------------------------+


