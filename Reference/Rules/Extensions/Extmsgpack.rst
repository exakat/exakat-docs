.. _extensions-extmsgpack:

.. _ext-msgpack:

ext/msgpack
+++++++++++

.. meta\:\:
	:description:
		ext/msgpack: Extension msgPack.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/msgpack
	:twitter:description: ext/msgpack: Extension msgPack
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/msgpack
	:og:type: article
	:og:description: Extension msgPack
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extmsgpack.html
	:og:locale: en
  Extension msgPack.

This extension provide API for handling MessagePack serialization, both encoding and decoding.

.. code-block:: php
   
   <?php
   
       $serialized = msgpack_serialize(array('a' => true, 'b' => 4));
       $unserialized = msgpack_unserialize($serialized);
   
   ?>

See also `msgpack for PHP <https://github.com/msgpack/msgpack-php>`_ and `MessagePack <https://msgpack.org/>`_.

Connex PHP features
-------------------

  + `format <https://php-dictionary.readthedocs.io/en/latest/dictionary/format.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extmsgpack                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.5                                                                                                                                                                                   |
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


