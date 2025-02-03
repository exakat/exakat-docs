.. _extensions-extprotobuf:

.. _ext-protobuf:

ext/protobuf
++++++++++++

.. meta::
	:description:
		ext/protobuf: Extension Protobuf.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/protobuf
	:twitter:description: ext/protobuf: Extension Protobuf
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/protobuf
	:og:type: article
	:og:description: Extension Protobuf
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/protobuf.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extprotobuf.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extprotobuf.html","name":"ext\/protobuf","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension Protobuf","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/protobuf.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Extension Protobuf.

Protocol Buffers (a.k.a., protobuf) are Google's language-neutral, platform-neutral, extensible mechanism for serializing structured data.

.. code-block:: php
   
   <?php
   
   // Example extracted from https://developers.google.com/protocol-buffers/docs/reference/php-generated
   
   // given a simple message 
   //message Foo {}
   
   /*
   The protocol buffer compiler generates a PHP class called Foo. This class inherits from a common base class, Google\Protobuf\Internal\Message, which provides methods for encoding and decoding your message types, as shown in the following example:
   */
   
   $from = new Foo();
   $from->setInt32(1);
   $from->setString('a');
   $from->getRepeatedInt32()[] = 1;
   $from->getMapInt32Int32()[1] = 1;
   $data = $from->serializeToString();
   try {
     $to->mergeFromString($data);
   } catch (Exception $e) {
     // Handle parsing error from invalid data.
     ...
   }
   
   ?>

See also `Protocol Buffers <https://developers.google.com/protocol-buffers>`_, `PHP Protocol Buffers <https://github.com/protocolbuffers/protobuf>`_ and `protobuf-php on packagist <https://github.com/protocolbuffers/protobuf-php>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extprotobuf                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


