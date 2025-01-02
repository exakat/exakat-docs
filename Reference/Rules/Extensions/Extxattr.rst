.. _extensions-extxattr:

.. _ext-xattr:

ext/xattr
+++++++++

.. meta::
	:description:
		ext/xattr: Extensions xattr.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/xattr
	:twitter:description: ext/xattr: Extensions xattr
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/xattr
	:og:type: article
	:og:description: Extensions xattr
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/xattr.html
	:og:locale: en
Extensions xattr.

The xattr extension allows for the manipulation of extended attributes on a filesystem.

.. code-block:: php
   
   <?php
   $file = 'my_favourite_song.wav';
   xattr_set($file, 'Artist', 'Someone');
   xattr_set($file, 'My ranking', 'Good');
   xattr_set($file, 'Listen count', '34');
   
   /* ... other code ... */
   
   printf('You\'ve played this song %d times', xattr_get($file, 'Listen count')); 
   ?>

See also `xattr <https://www.php.net/manual/en/book.xattr.php>`_ and `Extended attributres <https://en.wikipedia.org/wiki/Extended_file_attributes>`_.

Connex PHP features
-------------------

  + `file <https://php-dictionary.readthedocs.io/en/latest/dictionary/file.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extxattr                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.4                                                                                                                                                                                  |
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


