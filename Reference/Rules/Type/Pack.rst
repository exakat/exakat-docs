.. _type-pack:

.. _pack-format-inventory:

Pack Format Inventory
+++++++++++++++++++++

.. meta::
	:description:
		Pack Format Inventory: All format used in the code with pack() and unpack().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Pack Format Inventory
	:twitter:description: Pack Format Inventory: All format used in the code with pack() and unpack()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Pack Format Inventory
	:og:type: article
	:og:description: All format used in the code with pack() and unpack()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Pack Format Inventory.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Pack.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Pack.html","name":"Pack Format Inventory","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"All format used in the code with pack() and unpack()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Pack Format Inventory.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>All format used in the code with `pack() <https://www.php.net/pack>`_ and `unpack() <https://www.php.net/unpack>`_.

.. code-block:: php
   
   <?php
   
   $binarydata = "\x04\x00\xa0\x00";
   $array = unpack("cn", $binarydata);
   $initial = pack("cn", ...$array);
   
   ?>

See also `pack() <https://www.php.net/pack>`_.

Related PHP errors 
-------------------

  + `Type z: unknown format code <https://php-errors.readthedocs.io/en/latest/messages/type-%25c%3A-unknown-format-code.html>`_



Connex PHP features
-------------------

  + `pack <https://php-dictionary.readthedocs.io/en/latest/dictionary/pack.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/Pack                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.0                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


