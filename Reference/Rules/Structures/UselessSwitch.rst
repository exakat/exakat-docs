.. _structures-uselessswitch:

.. _useless-switch:

Useless Switch
++++++++++++++

.. meta::
	:description:
		Useless Switch: This switch has only one case.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Switch
	:twitter:description: Useless Switch: This switch has only one case
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Switch
	:og:type: article
	:og:description: This switch has only one case
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Switch.html
	:og:locale: en
This switch has only one case. It may very well be replaced by a ifthen structure.

.. code-block:: php
   
   <?php
   switch($a) {
       case 1:
           doSomething();
           break;
   }
   
   // Same as 
   
   if ($a == 1) {
       doSomething();
   }
   ?>
Connex PHP features
-------------------

  + `switch <https://php-dictionary.readthedocs.io/en/latest/dictionary/switch.ini.html>`_


Suggestions
___________

* Turn the switch into a if/then for better readability
* Add other cases to the switch, making it adapted to the situation




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessSwitch                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpdocumentor-structures-uselessswitch`, :ref:`case-dolphin-structures-uselessswitch`                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


