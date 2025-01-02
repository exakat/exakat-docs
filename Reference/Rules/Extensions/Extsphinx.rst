.. _extensions-extsphinx:

.. _ext-sphinx:

ext/sphinx
++++++++++

.. meta::
	:description:
		ext/sphinx: Extension for the Sphinx search server.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/sphinx
	:twitter:description: ext/sphinx: Extension for the Sphinx search server
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/sphinx
	:og:type: article
	:og:description: Extension for the Sphinx search server
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/sphinx.html
	:og:locale: en
Extension for the Sphinx search server.

This extension provides bindings for Sphinx search client library.

.. code-block:: php
   
   <?php
   
   $s = new SphinxClient;
   $s->setServer("localhost", 6712);
   $s->setMatchMode(SPH_MATCH_ANY);
   $s->setMaxQueryTime(3);
   
   $result = $s->query("test");
   
   var_dump($result);
   
   ?>

See also `Sphinx Client <https://www.php.net/manual/en/book.sphinx.php>`_ and `Sphinx Search <http://sphinxsearch.com/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extsphinx                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.3                                                                                                                                                                                  |
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


