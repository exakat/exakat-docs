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
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Security/GPRAliases.html
	:og:locale: en
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


