.. _php-gotonames:

.. _goto-names:

Goto Names
++++++++++

.. meta::
	:description:
		Goto Names: This rule lists of all goto labels used in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Goto Names
	:twitter:description: Goto Names: This rule lists of all goto labels used in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Goto Names
	:og:type: article
	:og:description: This rule lists of all goto labels used in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Goto Names.html
	:og:locale: en
This rule lists of all goto labels used in the code. The labels must match a goto call, although it is possible to create a label without a goto.

.. code-block:: php
   
   <?php
   
   GOTO_NAME_1: 
   
   // reports the usage of GOTO_NAME_1
   goto GOTO_NAME_1;
   
   UNUSED_GOTO_NAME_1: 
   
   ?>

See also `goto <https://www.php.net/goto>`_.

Connex PHP features
-------------------

  + `goto <https://php-dictionary.readthedocs.io/en/latest/dictionary/goto.ini.html>`_
  + `label <https://php-dictionary.readthedocs.io/en/latest/dictionary/label.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Gotonames                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-goto <https://github.com/dseguy/clearPHP/tree/master/rules/no-goto.md>`__                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


