.. _structures-dynamiccalls:

.. _dynamic-calls:

Dynamic Calls
+++++++++++++

.. meta::
	:description:
		Dynamic Calls: This rule lists all dynamic calls.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dynamic Calls
	:twitter:description: Dynamic Calls: This rule lists all dynamic calls
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dynamic Calls
	:og:type: article
	:og:description: This rule lists all dynamic calls
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dynamic Calls.html
	:og:locale: en
This rule lists all dynamic calls. This is convenient when one has to review them manually.

Only the dynamic call is listed : the sources are left in their context.


.. code-block:: php
   
   <?php
   
   $a = 'b';
   
   // Dynamic call of a constant
   echo constant($a);
   
   // Dynamic variables
   $$a = 2;
   echo $b;
   
   // Dynamic call of a function
   $a('b'); 
   
   // Dynamic call of a method
   $object->$a('b'); 
   
   // Dynamic call of a static method
   A::$a('b'); 
   
   ?>
Connex PHP features
-------------------

  + `dynamic-call <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-call.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DynamicCalls                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


