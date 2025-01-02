.. _interfaces-coulduseinterface:

.. _forgotten-interface:

Forgotten Interface
+++++++++++++++++++

.. meta::
	:description:
		Forgotten Interface: The following classes have been found implementing an interface's methods, though it doesn't explicitly implements this interface.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Forgotten Interface
	:twitter:description: Forgotten Interface: The following classes have been found implementing an interface's methods, though it doesn't explicitly implements this interface
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Forgotten Interface
	:og:type: article
	:og:description: The following classes have been found implementing an interface's methods, though it doesn't explicitly implements this interface
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Forgotten Interface.html
	:og:locale: en
The following classes have been found implementing an interface's methods, though it doesn't explicitly implements this interface. This may have been forgotten.

.. code-block:: php
   
   <?php
   
   interface i {
       function i(); 
   }
   
   // i is not implemented and declared
   class foo {
       function i() {}
       function j() {}
   }
   
   // i is implemented and declared
   class foo implements i {
       function i() {}
       function j() {}
   }
   
   ?>

See also :ref:`Could Use Trait <could-use-trait>`.

Connex PHP features
-------------------

  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_
  + `ducktyping <https://php-dictionary.readthedocs.io/en/latest/dictionary/ducktyping.ini.html>`_


Suggestions
___________

* Mention interfaces explicitly whenever possible




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/CouldUseInterface                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.7                                                                                                                  |
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


