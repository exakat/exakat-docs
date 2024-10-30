.. _php-hasvirtualproperty:

.. _has-virtual-property:

Has Virtual Property
++++++++++++++++++++

  Virtual properties are properties with hooks, which do not rely on storage, but process values stored somewhere else.

Virtual proeprties are akin to view, in SQL, where columns are calculated on the fly. 


.. code-block:: php
   
   <?php
   
   class x {
   	// This property doesn't store any data
   	private $random {
   		get { return rand(0, 10); }
   		set { }
   	}
   
   	// This property rely on another property
   	// here for history reasons
   	private $legacy {
   		get { return $this->random; }
   		set { }
   	}
   
   }
   
   ?>
Connex PHP features
-------------------

  + `hook <https://php-dictionary.readthedocs.io/en/latest/dictionary/hook.ini.html>`_
  + `virtual-property <https://php-dictionary.readthedocs.io/en/latest/dictionary/virtual-property.ini.html>`_


Specs
_____

+--------------+--------------------------+
| Short name   | Php/HasVirtualProperty   |
+--------------+--------------------------+
| Rulesets     | :ref:`All <ruleset-All>` |
+--------------+--------------------------+
| Exakat since | 2.6.8                    |
+--------------+--------------------------+
| Severity     | Minor                    |
+--------------+--------------------------+
| Time To Fix  | Quick (30 mins)          |
+--------------+--------------------------+
| Precision    | Unknown                  |
+--------------+--------------------------+
| Available in |                          |
+--------------+--------------------------+


