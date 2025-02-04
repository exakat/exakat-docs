.. _type-path:


.. _path-lists:

Path lists
++++++++++

.. meta::
	:description:
		Path lists: List of all paths that were found in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Path lists
	:twitter:description: Path lists: List of all paths that were found in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Path lists
	:og:type: article
	:og:description: List of all paths that were found in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Path lists.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Path.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Path.html","name":"Path lists","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"List of all paths that were found in the code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Path lists.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

List of all paths that were found in the code.

Path are identified with this regex : ``^(.*/)([^/]*)\.\w+$``. In particular, the `directory <https://www.php.net/directory>`_ delimiter is ``/`` : Windows delimiter ``\`` are not detected. 
URL are ignored when the protocol is present in the literal : ``http://www.example.`com <https://www.php.net/com>`_`` is not mistaken with a file.

.. code-block:: php
   
   <?php
   
   // the first argument is recognized as an URL
   fopen('/tmp/my/file.txt', 'r+');
   
   // the string argument  is recognized as an URL
   $source = 'https://www.other-example.com/';
   
   ?>

See also `Dir predefined constants <https://www.php.net/manual/en/dir.constants.php>`_ and `Supported Protocols and Wrappers <https://www.php.net/manual/en/wrappers.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/Path                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.8                                                                                                                                                                                   |
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


