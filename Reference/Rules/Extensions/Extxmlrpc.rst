.. _extensions-extxmlrpc:


.. _ext-xmlrpc:

ext/xmlrpc
++++++++++

.. meta::
	:description:
		ext/xmlrpc: Extension ext/xmlrpc.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/xmlrpc
	:twitter:description: ext/xmlrpc: Extension ext/xmlrpc
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/xmlrpc
	:og:type: article
	:og:description: Extension ext/xmlrpc
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/xmlrpc.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extxmlrpc.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extxmlrpc.html","name":"ext\/xmlrpc","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension ext\/xmlrpc","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/xmlrpc.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension ext/xmlrpc.

This extension can be used to write XML-RPC servers and clients.

.. code-block:: php
   
   <?php
   $request = xmlrpc_encode_request('method', array(1, 2, 3));
   $context = stream_context_create(array('http' => array(
       'method' => 'POST',
       'header' => 'Content-Type: text/xml',
       'content' => $request
   )));
   $file = file_get_contents('http://www.example.com/xmlrpc', false, $context);
   $response = xmlrpc_decode($file);
   if ($response && xmlrpc_is_fault($response)) {
       trigger_error('xmlrpc: '.$response['faultString'].' ('.$response['faultCode']));
   } else {
       print_r($response);
   }
   ?>

See also `XML-RPC <http://www.php.net/manual/en/book.xmlrpc.php>`_.

Connex PHP features
-------------------

  + `rpc <https://php-dictionary.readthedocs.io/en/latest/dictionary/rpc.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extxmlrpc                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


