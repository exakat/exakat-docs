.. _dump-indentationlevels:

.. _indentation-levels:

Indentation Levels
++++++++++++++++++

.. meta::
	:description:
		Indentation Levels: Collect all level of indentations for methods and functions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Indentation Levels
	:twitter:description: Indentation Levels: Collect all level of indentations for methods and functions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Indentation Levels
	:og:type: article
	:og:description: Collect all level of indentations for methods and functions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Indentation Levels.html
	:og:locale: en
Collect all level of indentations for methods and functions. Inside methods, indentation level raises for structures such as switch, `match() <https://www.php.net/manual/en/control-structures.match.php>`_, closures, ifthen, and loops. It is recommended to avoid going too high in the levels, as the code becomes less readable.

.. code-block:: php
   
   <?php
   
   function foo() {
       $a = 1; // level 1
       if ($b == 2) {
           $c = 1; // level 2
       }
       $d = 4; // level 1
   }
   
   ?>
Connex PHP features
-------------------

  + `indentation <https://php-dictionary.readthedocs.io/en/latest/dictionary/indentation.ini.html>`_
  + `inclusion <https://php-dictionary.readthedocs.io/en/latest/dictionary/inclusion.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/IndentationLevels                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                                                                                   |
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


