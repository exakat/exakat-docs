.. _extensions-extigbinary:

.. _ext-igbinary:

ext/igbinary
++++++++++++

.. meta::
	:description:
		ext/igbinary: Extension igbinary.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/igbinary
	:twitter:description: ext/igbinary: Extension igbinary
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/igbinary
	:og:type: article
	:og:description: Extension igbinary
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/igbinary.html
	:og:locale: en
Extension igbinary. 

igbinary is a drop in replacement for the standard php serializer. Instead of time and space consuming textual representation, igbinary stores php data structures in compact binary form.

.. code-block:: php
   
   <?php
   	$serialized = igbinary_serialize($variable);
   	$unserialized = igbinary_unserialize($serialized);
   ?>

See also `igbinary <https://github.com/igbinary/igbinary/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extigbinary                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.6                                                                                                                                                                                   |
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


