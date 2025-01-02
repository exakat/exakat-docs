.. _php-hasvirtualproperty:

.. _has-virtual-property:

Has Virtual Property
++++++++++++++++++++

.. meta::
	:description:
		Has Virtual Property: Virtual properties are properties with hooks, which do not rely on storage, but process values stored somewhere else.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Has Virtual Property
	:twitter:description: Has Virtual Property: Virtual properties are properties with hooks, which do not rely on storage, but process values stored somewhere else
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Has Virtual Property
	:og:type: article
	:og:description: Virtual properties are properties with hooks, which do not rely on storage, but process values stored somewhere else
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Has Virtual Property.html
	:og:locale: en
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

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/HasVirtualProperty                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.4 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


