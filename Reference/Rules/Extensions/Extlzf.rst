.. _extensions-extlzf:

.. _ext-lzf:

ext/lzf
+++++++

.. meta::
	:description:
		ext/lzf: Extension LZF.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/lzf
	:twitter:description: ext/lzf: Extension LZF
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/lzf
	:og:type: article
	:og:description: Extension LZF
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/lzf.html
	:og:locale: en
Extension LZF.

LZF is a very fast compression algorithm, ideal for saving space with only slight speed cost. It can be optimized for speed or space at the time of compilation.

.. code-block:: php
   
   <?php
   $compressed = lzf_compress("This is test of LZF extension");
   
   echo base64_encode($compressed);
   ?>

See also `lzf <https://www.php.net/lzf>`_ and `liblzf <http://oldhome.schmorp.de/marc/liblzf.html>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extlzf                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.5                                                                                                                                                                                   |
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


