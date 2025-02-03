.. _extensions-extgrpc:


.. _ext-grpc:

ext/grpc
++++++++

.. meta::
	:description:
		ext/grpc: Extension for GRPC : A high performance, open-source universal RPC framework.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/grpc
	:twitter:description: ext/grpc: Extension for GRPC : A high performance, open-source universal RPC framework
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/grpc
	:og:type: article
	:og:description: Extension for GRPC : A high performance, open-source universal RPC framework
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/grpc.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extgrpc.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extgrpc.html","name":"ext\/grpc","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension for GRPC : A high performance, open-source universal RPC framework","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/grpc.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension for GRPC : A high performance, open-source universal RPC framework.

.. code-block:: php
   
   <?php
   
   //https://github.com/grpc/grpc/blob/master/examples/php/greeter_client.php
   
   require dirname(__FILE__).'/vendor/autoload.php';
   // The following includes are needed when using protobuf 3.1.0
   // and will suppress warnings when using protobuf 3.2.0+
   @include_once dirname(__FILE__).'/helloworld.pb.php';
   @include_once dirname(__FILE__).'/helloworld_grpc_pb.php';
   function greet($name)
   {
       $client = new Helloworld\GreeterClient('localhost:50051', [
           'credentials' => Grpc\ChannelCredentials::createInsecure(),
       ]);
       $request = new Helloworld\HelloRequest();
       $request->setName($name);
       list($reply, $status) = $client->SayHello($request)->wait();
       $message = $reply->getMessage();
       return $message;
   }
   $name = !empty($argv[1]) ? $argv[1] : 'world';
   echo greet($name)."\n";
   
   ?>

See also `GRPC <http://www.grpc.io/>`_ and `GRPC on PECL <https://pecl.php.net/package/gRPC>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extgrpc                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.3                                                                                                                                                                                  |
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


