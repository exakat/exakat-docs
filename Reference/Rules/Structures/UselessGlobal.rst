.. _structures-uselessglobal:

.. _useless-global:

Useless Global
++++++++++++++

.. meta::
	:description:
		Useless Global: Global are useless in two cases.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Global
	:twitter:description: Useless Global: Global are useless in two cases
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Global
	:og:type: article
	:og:description: Global are useless in two cases
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Global.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UselessGlobal.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UselessGlobal.html","name":"Useless Global","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Global are useless in two cases","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless Global.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Global are useless in two cases. First, on super-globals, which are always globals, like `$_GET <https://www.php.net/manual/en/reserved.variables.get.php>`_; secondly, on variables that are not used.
Also, PHP has superglobals, a special team of variables that are always available, whatever the context. 
They are : $GLOBALS, $_SERVER, `$_GET <https://www.php.net/manual/en/reserved.variables.get.php>`_, `$_POST <https://www.php.net/manual/en/reserved.variables.post.php>`_, $_FILES, $_COOKIE, $_SESSION, `$_REQUEST <https://www.php.net/manual/en/reserved.variables.request.php>`_ and `$_ENV <https://www.php.net/manual/en/reserved.variables.env.php>`_.

.. code-block:: php
   
   <?php
   
   // $_POST is already a global : it is in fact a global everywhere
   global $_POST;
   
   // $unused is useless
   function foo() {
       global $used, $unused;
       
       ++$used;
   }
   
   ?>
Connex PHP features
-------------------

  + `super-global <https://php-dictionary.readthedocs.io/en/latest/dictionary/super-global.ini.html>`_
  + `$_get <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24_get.ini.html>`_
  + `$_post <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24_post.ini.html>`_
  + `$_server <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24_server.ini.html>`_
  + `$globals <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24globals.ini.html>`_
  + `$_files <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24_files.ini.html>`_
  + `$_cookie <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24_cookie.ini.html>`_
  + `$_request <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24_request.ini.html>`_
  + `$_env <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24_env.ini.html>`_


Suggestions
___________

* Drop the global expression




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessGlobal                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zencart-structures-uselessglobal`, :ref:`case-humo-gen-structures-uselessglobal`                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


