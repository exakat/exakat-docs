.. _extensions-extncurses:

.. _ext-ncurses:

ext/ncurses
+++++++++++

.. meta::
	:description:
		ext/ncurses: Extension ncurses (CLI).
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/ncurses
	:twitter:description: ext/ncurses: Extension ncurses (CLI)
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/ncurses
	:og:type: article
	:og:description: Extension ncurses (CLI)
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/ncurses.html
	:og:locale: en
Extension ncurses (CLI).

ncurses (new curses) is a free software emulation of curses in System V Rel 4.0 (and above).

.. code-block:: php
   
   <?php
   ncurses_init();
   ncurses_start_color();
   ncurses_init_pair(1, NCURSES_COLOR_GREEN, NCURSES_COLOR_BLACK);
   ncurses_init_pair(2, NCURSES_COLOR_RED,   NCURSES_COLOR_BLACK);
   ncurses_init_pair(3, NCURSES_COLOR_WHITE, NCURSES_COLOR_BLACK);
   ncurses_color_set(1);
   ncurses_addstr('OK   ');
   ncurses_color_set(3);
   ncurses_addstr('Success!'.PHP_EOL);
   ncurses_color_set(2);
   ncurses_addstr('FAIL ');
   ncurses_color_set(3);
   ncurses_addstr('Success!'.PHP_EOL);
   ?>

See also `Ncurses Terminal Screen Control <https://www.php.net/manual/en/book.ncurses.php>`_ and `Ncurses <https://www.gnu.org/software/ncurses/ncurses.html>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extncurses                                                                                                                                                                   |
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


