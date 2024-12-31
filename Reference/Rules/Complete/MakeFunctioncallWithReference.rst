.. _complete-makefunctioncallwithreference:

.. _make-functioncall-with-reference:

Make Functioncall With Reference
++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Make Functioncall With Reference: Mark parameters as ``isModified`` if the functioncall uses reference.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Make Functioncall With Reference
	:twitter:description: Make Functioncall With Reference: Mark parameters as ``isModified`` if the functioncall uses reference
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Make Functioncall With Reference
	:og:type: article
	:og:description: Mark parameters as ``isModified`` if the functioncall uses reference
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Complete/MakeFunctioncallWithReference.html
	:og:locale: en
  Mark parameters as ``isModified`` if the functioncall uses reference.

This works on PHP native functions and custom functions.

This doesn't work on dynamic calls nor methods yet.

.. code-block:: php
   
   <?php
   
   function foo($a, &$b) {}
   
   // $b is marked as modified
   foo($a, $b);
   
   ?>
Connex PHP features
-------------------

  + `reference <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/MakeFunctioncallWithReference                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`NoDoc <ruleset-NoDoc>`                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.7                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


