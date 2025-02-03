.. _extensions-extuuid:

.. _ext-uuid:

ext/uuid
++++++++

.. meta::
	:description:
		ext/uuid: Extension ``UUID``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/uuid
	:twitter:description: ext/uuid: Extension ``UUID``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/uuid
	:og:type: article
	:og:description: Extension ``UUID``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/uuid.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extuuid.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extuuid.html","name":"ext\/uuid","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension ``UUID``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/uuid.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Extension ``UUID``. A universally unique identifier (UUID) is a 128-bit number used to identify information in computer systems.

An interface to the libuuid system library. The libuuid library is used to generate unique identifiers for objects that may be accessible beyond the local system. The Linux implementation was created to uniquely identify ext2 filesystems created by a machine. This library generates UUIDs compatible with those created by the Open Software Foundation (OSF) Distributed Computing Environment (DCE) utility uuidgen.

.. code-block:: php
   
   <?php
       // example from the test suitee of the extension.
       
       // check basic format of generated UUIDs
       $uuid = uuid_create();
       if (preg_match("/[[:xdigit:]]{8}-[[:xdigit:]]{4}-[[:xdigit:]]{4}-[[:xdigit:]]{4}-[[:xdigit:]]{12}/", $uuid)) {
               echo "basic format ok\n";
       } else {
               echo "basic UUID format check failed, generated UUID was $uuid\n";
       }
       
   ?>

See also `libuuid <https://linux.die.net/man/3/libuuid>`_ and `ext/uuid <https://github.com/php/pecl-networking-uuid>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extuuid                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.9                                                                                                                                                                                   |
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


