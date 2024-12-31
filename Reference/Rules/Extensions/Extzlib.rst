.. _extensions-extzlib:

.. _ext-zlib:

ext/zlib
++++++++

.. meta\:\:
	:description:
		ext/zlib: Extension ext/zlib.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/zlib
	:twitter:description: ext/zlib: Extension ext/zlib
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/zlib
	:og:type: article
	:og:description: Extension ext/zlib
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extzlib.html
	:og:locale: en
  Extension ext/zlib.

.. code-block:: php
   
   <?php
   
   $filename = tempnam('/tmp', 'zlibtest') . '.gz';
   echo "<html>\n<head></head>\n<body>\n<pre>\n";
   $s = "Only a test, test, test, test, test, test, test, test!\n";
   
   // open file for writing with maximum compression
   $zp = gzopen($filename, 'w9');
   
   // write string to file
   gzwrite($zp, $s);
   
   // close file
   gzclose($zp);
   
   ?>

See also `Zlib <https://www.php.net/manual/en/book.zlib.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extzlib                                                                                                                                                                      |
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


