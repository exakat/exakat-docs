.. _extensions-extphar:

.. _ext-phar:

ext/phar
++++++++

.. meta\:\:
	:description:
		ext/phar: Extension phar.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/phar
	:twitter:description: ext/phar: Extension phar
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/phar
	:og:type: article
	:og:description: Extension phar
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extphar.html
	:og:locale: en
  Extension `phar <https://www.php.net/phar>`_.

The `phar <https://www.php.net/phar>`_ extension provides a way to put entire PHP applications into a single file called a ``phar`` (PHP Archive) for easy distribution and installation.

.. code-block:: php
   
   <?php
   try {
       $p = new Phar('/path/to/my.phar', 0, 'my.phar');
       $p['myfile.txt'] = 'hi';
       $file = $p['myfile.txt'];
       var_dump($file->isCompressed(Phar::BZ2));
       $p['myfile.txt']->compress(Phar::BZ2);
       var_dump($file->isCompressed(Phar::BZ2));
   } catch (Exception $e) {
       echo 'Create/modify operations on my.phar failed: ', $e;
   }
   ?>

See also `phar <http://www.php.net/manual/en/book.phar.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extphar                                                                                                                                                                      |
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


