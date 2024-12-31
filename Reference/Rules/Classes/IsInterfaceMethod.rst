.. _classes-isinterfacemethod:

.. _is-interface-method:

Is Interface Method
+++++++++++++++++++

.. meta\:\:
	:description:
		Is Interface Method: Mark a method as part of an interface that the current class implements.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Is Interface Method
	:twitter:description: Is Interface Method: Mark a method as part of an interface that the current class implements
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Is Interface Method
	:og:type: article
	:og:description: Mark a method as part of an interface that the current class implements
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/IsInterfaceMethod.html
	:og:locale: en
  Mark a method as part of an interface that the current class implements.

.. code-block:: php
   
   <?php
   
   interface i {
       function i20();
   }
   
   class x implements i {
       // This is an interface method
       function i20() {}
   
       // This is not an interface method
       function x20() {}
   }
   
   ?>
Connex PHP features
-------------------

  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/IsInterfaceMethod                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


