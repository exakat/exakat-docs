.. _dump-collectforeachfavorite:

.. _foreach()-favorite:

Foreach() Favorite
++++++++++++++++++

.. meta::
	:description:
		Foreach() Favorite: Collect the name used in foreach() loops.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Foreach() Favorite
	:twitter:description: Foreach() Favorite: Collect the name used in foreach() loops
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Foreach() Favorite
	:og:type: article
	:og:description: Collect the name used in foreach() loops
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Dump/CollectForeachFavorite.html
	:og:locale: en
Collect the name used in `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loops. Then, sorts them in order of popularity.

.. code-block:: php
   
   <?php
   
   // collect $k, $v
   foreach($array as $k => $v) { }
   
   // collect $k, $v1, $v2
   foreach($array as $k => [$v1, $v2]) { }
   
   ?>
Connex PHP features
-------------------

  + `foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectForeachFavorite                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.7                                                                                                                                                                                   |
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


