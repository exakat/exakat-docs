.. _php-php80removesresources:

.. _php-8.0-resources-turned-into-objects:

PHP 8.0 Resources Turned Into Objects
+++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		PHP 8.0 Resources Turned Into Objects: Multiple PHP native functions now return objects, not resources.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 8.0 Resources Turned Into Objects
	:twitter:description: PHP 8.0 Resources Turned Into Objects: Multiple PHP native functions now return objects, not resources
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 8.0 Resources Turned Into Objects
	:og:type: article
	:og:description: Multiple PHP native functions now return objects, not resources
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP 8.0 Resources Turned Into Objects.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php80RemovesResources.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php80RemovesResources.html","name":"PHP 8.0 Resources Turned Into Objects","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"Multiple PHP native functions now return objects, not resources","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP 8.0 Resources Turned Into Objects.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Multiple PHP native functions now return objects, not resources. Any check on those values with `is_resource() <https://www.php.net/is_resource>`_ is now going to fail.

The affected functions are the following : 

+ `curl_init() <https://www.php.net/curl_init>`_
+ `curl_multi_init() <https://www.php.net/curl_multi_init>`_
+ `curl_share_init() <https://www.php.net/curl_share_init>`_
+ `deflate_init() <https://www.php.net/deflate_init>`_
+ `enchant_broker_init() <https://www.php.net/enchant_broker_init>`_
+ `enchant_broker_request_dict() <https://www.php.net/enchant_broker_request_dict>`_
+ `enchant_broker_request_pwl_dict() <https://www.php.net/enchant_broker_request_pwl_dict>`_
+ `inflate_init() <https://www.php.net/inflate_init>`_
+ `msg_get_queue() <https://www.php.net/msg_get_queue>`_
+ `openssl_csr_new() <https://www.php.net/openssl_csr_new>`_
+ `openssl_csr_sign() <https://www.php.net/openssl_csr_sign>`_
+ `openssl_pkey_new() <https://www.php.net/openssl_pkey_new>`_
+ `openssl_x509_read() <https://www.php.net/openssl_x509_read>`_
+ `sem_get() <https://www.php.net/sem_get>`_
+ `shm_attach() <https://www.php.net/shm_attach>`_
+ `shmop_open() <https://www.php.net/shmop_open>`_
+ `socket_accept() <https://www.php.net/socket_accept>`_
+ `socket_addrinfo_bind() <https://www.php.net/socket_addrinfo_bind>`_
+ `socket_addrinfo_connect() <https://www.php.net/socket_addrinfo_connect>`_
+ `socket_create_listen() <https://www.php.net/socket_create_listen>`_
+ `socket_create() <https://www.php.net/socket_create>`_
+ `socket_import_stream() <https://www.php.net/socket_import_stream>`_
+ socket_wsaprotocol_info_import()
+ `xml_parser_create_ns() <https://www.php.net/xml_parser_create_ns>`_
+ `xml_parser_create() <https://www.php.net/xml_parser_create>`_

See also `Resource to object migration <https://www.php.net/manual/en/migration80.incompatible.php#migration81.incompatible.resource2object>`_.

Connex PHP features
-------------------

  + `resource <https://php-dictionary.readthedocs.io/en/latest/dictionary/resource.ini.html>`_


Suggestions
___________

* Change the condition from is_resource() to instanceof




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php80RemovesResources                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


