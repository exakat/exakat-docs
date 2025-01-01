.. _extensions-extfileinfo:

.. _ext-fileinfo:

ext/fileinfo
++++++++++++

.. meta::
	:description:
		ext/fileinfo: Extension ext/fileinfo.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/fileinfo
	:twitter:description: ext/fileinfo: Extension ext/fileinfo
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/fileinfo
	:og:type: article
	:og:description: Extension ext/fileinfo
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extfileinfo.html
	:og:locale: en
Extension ext/fileinfo.

This module guesses the content type and encoding of a file by looking for certain magic byte sequences at specific positions within the file.

.. code-block:: php
   
   <?php
   $finfo = finfo_open(FILEINFO_MIME_TYPE); // return mime type ala mimetype extension
   foreach (glob('*') as $filename) {
       echo finfo_file($finfo, $filename) . PHP_EOL;
   }
   finfo_close($finfo);
   ?>

See also `Filinfo <https://www.php.net/manual/en/book.fileinfo.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extfileinfo                                                                                                                                                                  |
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


