.. _type-protocols:


.. _protocol-lists:

Protocol lists
++++++++++++++

.. meta::
	:description:
		Protocol lists: List of all protocols that were found in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Protocol lists
	:twitter:description: Protocol lists: List of all protocols that were found in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Protocol lists
	:og:type: article
	:og:description: List of all protocols that were found in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Protocol lists.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Protocols.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Protocols.html","name":"Protocol lists","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"List of all protocols that were found in the code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Protocol lists.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

List of all protocols that were found in the code.

From the manual : PHP comes with many built-in wrappers for various URL-style protocols for use with the filesystem functions such as `fopen() <https://www.php.net/fopen>`_, `copy() <https://www.php.net/copy>`_, `file_exists() <https://www.php.net/file_exists>`_ and `filesize() <https://www.php.net/filesize>`_.

.. code-block:: php
   
   <?php
   // Example from the PHP manual, with the glob:// wrapper
   
   // Loop over all *.php files in ext/spl/examples/ directory
   // and print the filename and its size
   $it = new DirectoryIterator("glob://ext/spl/examples/*.php");
   foreach($it as $f) {
       printf("%s: %.1FK\n", $f->getFilename(), $f->getSize()/1024);
   }
   ?>

See also `Supported Protocols and Wrappers <https://www.php.net/manual/en/wrappers.php>`_.

Connex PHP features
-------------------

  + `Protocol <https://php-dictionary.readthedocs.io/en/latest/dictionary/protocol.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/Protocols                                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.3                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


