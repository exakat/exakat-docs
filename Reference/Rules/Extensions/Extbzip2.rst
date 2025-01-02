.. _extensions-extbzip2:

.. _ext-bzip2:

ext/bzip2
+++++++++

.. meta::
	:description:
		ext/bzip2: Extension ext/bzip2.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/bzip2
	:twitter:description: ext/bzip2: Extension ext/bzip2
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/bzip2
	:og:type: article
	:og:description: Extension ext/bzip2
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/bzip2.html
	:og:locale: en
Extension ext/bzip2.

Bzip2 Functions for PHP.

.. code-block:: php
   
   <?php
   
   $file = '/tmp/foo.bz2';
   $bz = bzopen($file, 'r') or die('Couldn\'t open $file for reading');
   
   bzclose($bz);
   
   ?>

See also `Bzip2 Functions <https://www.php.net/bzip2>`_ and `bzip2 <https://en.wikipedia.org/wiki/Bzip2>`_.

Connex PHP features
-------------------

  + `compression <https://php-dictionary.readthedocs.io/en/latest/dictionary/compression.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extbzip2                                                                                                                                                                     |
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


