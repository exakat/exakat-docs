.. _extensions-exttokyotyrant:

.. _ext-tokyotyrant:

ext/tokyotyrant
+++++++++++++++

.. meta::
	:description:
		ext/tokyotyrant: Extension for Tokyo Tyrant.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/tokyotyrant
	:twitter:description: ext/tokyotyrant: Extension for Tokyo Tyrant
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/tokyotyrant
	:og:type: article
	:og:description: Extension for Tokyo Tyrant
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Exttokyotyrant.html
	:og:locale: en
Extension for Tokyo Tyrant.

tokyo_tyrant extension provides a wrapper for Tokyo Tyrant client libraries.

.. code-block:: php
   
   <?php
   $tt = new TokyoTyrant("localhost");
   $tt->put("key", "value");
   echo $tt->get("key");
   ?>

See also `tokyo_tyrant <https://www.php.net/manual/en/book.tokyo-tyrant.php>`_ and `Tokyo cabinet <http://fallabs.com/tokyocabinet/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Exttokyotyrant                                                                                                                                                               |
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


