.. _extensions-extssh2:

.. _ext-ssh2:

ext/ssh2
++++++++

.. meta::
	:description:
		ext/ssh2: Extension ext/ssh2.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/ssh2
	:twitter:description: ext/ssh2: Extension ext/ssh2
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/ssh2
	:og:type: article
	:og:description: Extension ext/ssh2
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/ssh2.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extssh2.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extssh2.html","name":"ext\/ssh2","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension ext\/ssh2","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/ssh2.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Extension ext/ssh2.

.. code-block:: php
   
   <?php
   /* Notify the user if the server terminates the connection */
   function my_ssh_disconnect($reason, $message, $language) {
     printf("Server disconnected with reason code [%d] and message: %s\n",
            $reason, $message);
   }
   
   $methods = array(
     'kex' => 'diffie-hellman-group1-sha1',
     'client_to_server' => array(
       'crypt' => '3des-cbc',
       'comp' => 'none'),
     'server_to_client' => array(
       'crypt' => 'aes256-cbc,aes192-cbc,aes128-cbc',
       'comp' => 'none'));
   
   $callbacks = array('disconnect' => 'my_ssh_disconnect');
   
   $connection = ssh2_connect('shell.example.com', 22, $methods, $callbacks);
   if (!$connection) die('Connection failed');
   ?>

See also `SSH2 functions <https://www.php.net/manual/en/book.ssh2.php>`_ and `ext/ssh2 on PECL <http://pecl.php.net/package/ssh2>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extssh2                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
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


