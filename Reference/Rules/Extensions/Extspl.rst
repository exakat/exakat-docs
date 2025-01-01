.. _extensions-extspl:

.. _ext-spl:

ext/spl
+++++++

.. meta::
	:description:
		ext/spl: SPL extension.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/spl
	:twitter:description: ext/spl: SPL extension
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/spl
	:og:type: article
	:og:description: SPL extension
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extspl.html
	:og:locale: en
SPL extension.

The Standard PHP Library (SPL) is a collection of interfaces and classes that are meant to solve common problems.

.. code-block:: php
   
   <?php
   
   // Example with FilesystemIterator
   $files = new FilesystemIterator('/path/to/dir');
   foreach($files as $file) {
       echo $file->getFilename() . PHP_EOL;
   }
   
   ?>

See also `Standard PHP Library (SPL) <http://www.php.net/manual/en/book.spl.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extspl                                                                                                                                                                       |
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


