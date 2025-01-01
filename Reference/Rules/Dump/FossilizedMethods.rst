.. _dump-fossilizedmethods:

.. _fossilized-methods-list:

Fossilized Methods List
+++++++++++++++++++++++

.. meta::
	:description:
		Fossilized Methods List: This is the list of fossilized methods.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Fossilized Methods List
	:twitter:description: Fossilized Methods List: This is the list of fossilized methods
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Fossilized Methods List
	:og:type: article
	:og:description: This is the list of fossilized methods
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Dump/FossilizedMethods.html
	:og:locale: en
This is the list of fossilized methods. Those methods appears when they get tightly couple with a child or `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class, and cannot evolve anymore without making the rest of the family evolve also. They are now very difficult to update and usually, become inert.

.. code-block:: php
   
   <?php
   
   class x {
       function foo(int $a) : string {
           //...
       }
   }
   
   class y extends x {
       // this methods is fossilized, as its modification will trigger an update in the parent class
       function foo(int $a) : string {
           //...
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `fossilized-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/fossilized-method.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/FossilizedMethods                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.5                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


