.. _extensions-extvarnish:

.. _ext-varnish:

ext/varnish
+++++++++++

.. meta::
	:description:
		ext/varnish: Extension PHP for varnish.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/varnish
	:twitter:description: ext/varnish: Extension PHP for varnish
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/varnish
	:og:type: article
	:og:description: Extension PHP for varnish
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/varnish.html
	:og:locale: en
Extension PHP for varnish.

Varnish Cache is an open source, state of the art web application accelerator. The extension makes it possible to interact with a running varnish instance through TCP `socket <https://www.php.net/socket>`_ or shared memory.

.. code-block:: php
   
   <?php
       $args = array(
           VARNISH_CONFIG_HOST => '::1',
           VARNISH_CONFIG_PORT => 6082,
           VARNISH_CONFIG_SECRET => '5174826b-8595-4958-aa7a-0609632ad7ca',
           VARNISH_CONFIG_TIMEOUT => 300,
       );
       $va = new VarnishAdmin($args);
   ?>

See also `ext/varnish <https://www.php.net/manual/en/book.varnish.php>`_ and `pecl/Varnish <http://svn.php.net/viewvc/pecl/varnish/trunk/tests/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extvarnish                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.7                                                                                                                                                                                   |
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


