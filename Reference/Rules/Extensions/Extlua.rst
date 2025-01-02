.. _extensions-extlua:

.. _ext-lua:

ext/lua
+++++++

.. meta::
	:description:
		ext/lua: Extension Lua.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/lua
	:twitter:description: ext/lua: Extension Lua
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/lua
	:og:type: article
	:og:description: Extension Lua
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/lua.html
	:og:locale: en
Extension Lua.

'Lua is a powerful, fast, light-weight, embeddable scripting language.' This extension embeds the lua interpreter and offers an OO-API to lua variables and functions.

.. code-block:: php
   
   <?php
   $lua = new Lua();
   $lua->eval(<<<CODE
       print(2);
   CODE
   );
   ?>

See also `ext/lua manual <https://www.php.net/manual/en/book.lua.php>`_ and `LUA <https://www.lua.org/>`_.

Connex PHP features
-------------------

  + `pecl <https://php-dictionary.readthedocs.io/en/latest/dictionary/pecl.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extlua                                                                                                                                                                       |
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
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


