.. _security-gpraliases:


.. _gprc-aliases:

GPRC Aliases
++++++++++++


.. meta::

	:description:

		GPRC Aliases: The following variables are holding the content of $_GET, $_POST, $_REQUEST or $_COOKIE.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: GPRC Aliases

	:twitter:description: GPRC Aliases: The following variables are holding the content of $_GET, $_POST, $_REQUEST or $_COOKIE

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: GPRC Aliases

	:og:type: article

	:og:description: The following variables are holding the content of $_GET, $_POST, $_REQUEST or $_COOKIE

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/GPRC Aliases.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/GPRAliases.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/GPRAliases.html","name":"GPRC Aliases","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The following variables are holding the content of $_GET, $_POST, $_REQUEST or $_COOKIE","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/GPRC Aliases.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The following variables are holding the content of `$_GET <https://www.php.net/manual/en/reserved.variables.get.php>`_, `$_POST <https://www.php.net/manual/en/reserved.variables.post.php>`_, `$_REQUEST <https://www.php.net/manual/en/reserved.variables.request.php>`_ or $_COOKIE. They shouldn't be trusted, just like their original variables.

.. code-block:: php
   
   <?php
   
   $post = $_POST;
   
   foreach($post as $key => $var)  {
   	print $var;
   }
   
   ?>

See also `Superglobals <https://www.php.net/manual/en/language.variables.superglobals.php>`_.

Connex PHP features
-------------------

  + `superglobal <https://php-dictionary.readthedocs.io/en/latest/dictionary/superglobal.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/GPRAliases                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


