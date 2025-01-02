.. _php-dlusage:

.. _dl()-usage:

Dl() Usage
++++++++++

.. meta::
	:description:
		Dl() Usage: Dynamically load PHP extensions with dl().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dl() Usage
	:twitter:description: Dl() Usage: Dynamically load PHP extensions with dl()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dl() Usage
	:og:type: article
	:og:description: Dynamically load PHP extensions with dl()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dl() Usage.html
	:og:locale: en
Dynamically load PHP extensions with `dl() <https://www.php.net/dl>`_.

.. code-block:: php
   
   <?php
   
       // dynamically loading ext/vips
   	dl('vips.' . PHP_SHLIB_SUFFIX);
   
   ?>

See also `dl <http://www.php.net/dl>`_.

Connex PHP features
-------------------

  + `extension <https://php-dictionary.readthedocs.io/en/latest/dictionary/extension.ini.html>`_
  + `dynamic-loading <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-loading.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/DlUsage                                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                                                                                   |
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


