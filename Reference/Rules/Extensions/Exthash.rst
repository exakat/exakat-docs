.. _extensions-exthash:

.. _ext-hash:

ext/hash
++++++++

.. meta\:\:
	:description:
		ext/hash: Extension for HASH Message Digest Framework.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/hash
	:twitter:description: ext/hash: Extension for HASH Message Digest Framework
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/hash
	:og:type: article
	:og:description: Extension for HASH Message Digest Framework
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Exthash.html
	:og:locale: en
  Extension for HASH Message Digest Framework.

Message Digest (hash) `engine <https://www.php.net/engine>`_. Allows direct or incremental processing of arbitrary length messages using a variety of hashing algorithms.

.. code-block:: php
   
   <?php
   /* Create a file to calculate hash of */
   file_put_contents('example.txt', 'The quick brown fox jumped over the lazy dog.');
   
   echo hash_file('md5', 'example.txt');
   ?>

See also `HASH Message Digest Framework <http://www.php.net/manual/en/book.hash.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Exthash                                                                                                                                                                      |
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


