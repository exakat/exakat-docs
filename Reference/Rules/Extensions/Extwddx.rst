.. _extensions-extwddx:

.. _ext-wddx:

ext/wddx
++++++++

.. meta::
	:description:
		ext/wddx: Extension WDDX.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/wddx
	:twitter:description: ext/wddx: Extension WDDX
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/wddx
	:og:type: article
	:og:description: Extension WDDX
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/wddx.html
	:og:locale: en
Extension WDDX.

The Web Distributed Data Exchange, or WDDX, is a free, open XML-based technology that allows Web applications created with any platform to easily exchange data with one another over the Web.

.. code-block:: php
   
   <?php
     echo wddx_serialize_value("PHP to WDDX packet example", "PHP packet");
   ?>

See also `Wddx on PHP <https://www.php.net/manual/en/intro.wddx.php>`_ and `WDDX <http://www.openwddx.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extwddx                                                                                                                                                                      |
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


