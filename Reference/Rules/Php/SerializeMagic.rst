.. _php-serializemagic:


.. _serialize-magic-method:

Serialize Magic Method
++++++++++++++++++++++

.. meta::
	:description:
		Serialize Magic Method: Classes that defines __serialize() and __unserialize() are using Serialize Magic.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Serialize Magic Method
	:twitter:description: Serialize Magic Method: Classes that defines __serialize() and __unserialize() are using Serialize Magic
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Serialize Magic Method
	:og:type: article
	:og:description: Classes that defines __serialize() and __unserialize() are using Serialize Magic
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Serialize Magic Method.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/SerializeMagic.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/SerializeMagic.html","name":"Serialize Magic Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Classes that defines __serialize() and __unserialize() are using Serialize Magic","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Serialize Magic Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Classes that defines __serialize() and __unserialize() are using Serialize Magic.

Serialize magic methods were introduced in PHP 7.4, and are not effective before.

.. code-block:: php
   
   <?php
   
   class x {
       function __serialize() {}
       function __unserialize() {}
   }
   
   ?>

See also `New custom object serialization mechanism <https://wiki.php.net/rfc/custom_object_serialization>`_.

Connex PHP features
-------------------

  + `Serialization <https://php-dictionary.readthedocs.io/en/latest/dictionary/serialize.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/SerializeMagic                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


