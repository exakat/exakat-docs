.. _extensions-extreadline:

.. _ext-readline:

ext/readline
++++++++++++

.. meta\:\:
	:description:
		ext/readline: Extension readline.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/readline
	:twitter:description: ext/readline: Extension readline
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/readline
	:og:type: article
	:og:description: Extension readline
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extreadline.html
	:og:locale: en
  Extension readline.

The readline functions implement an interface to the GNU Readline library. These are functions that provide editable command lines.

.. code-block:: php
   
   <?php
   //get 3 commands from user
   for ($i=0; $i < 3; $i++) {
           $line = readline("Command: ");
           readline_add_history($line);
   }
   
   //dump history
   print_r(readline_list_history());
   
   //dump variables
   print_r(readline_info());
   ?>

See also `ext/readline <https://www.php.net/manual/en/book.readline.php>`_ and `The GNU Readline Library <https://tiswww.case.edu/php/chet/readline/rltop.html>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extreadline                                                                                                                                                                  |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


