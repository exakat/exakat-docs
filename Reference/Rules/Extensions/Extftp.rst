.. _extensions-extftp:

.. _ext-ftp:

ext/ftp
+++++++

.. meta::
	:description:
		ext/ftp: Extension FTP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/ftp
	:twitter:description: ext/ftp: Extension FTP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/ftp
	:og:type: article
	:og:description: Extension FTP
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/ftp.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extftp.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extftp.html","name":"ext\/ftp","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension FTP","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/ftp.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Extension FTP.

The functions in this extension implement client access to files servers speaking the File Transfer Protocol (FTP) as defined in `RFC 959 <http://www.faqs.org/rfcs/rfc959>`_.

.. code-block:: php
   
   <?php
   // set up basic connection
   $conn_id = ftp_connect($ftp_server); 
   
   // login with username and password
   $login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass); 
   
   // check connection
   if ((!$conn_id) || (!$login_result)) { 
       echo 'FTP connection has failed!';
       echo 'Attempted to connect to $ftp_server for user $ftp_user_name'; 
       exit; 
   } else {
       echo 'Connected to $ftp_server, for user $ftp_user_name';
   }
   
   // upload the file
   $upload = ftp_put($conn_id, $destination_file, $source_file, FTP_BINARY); 
   
   // check upload status
   if (!$upload) { 
       echo 'FTP upload has failed!';
   } else {
       echo 'Uploaded $source_file to $ftp_server as $destination_file';
   }
   
   // close the FTP stream 
   ftp_close($conn_id); 
   ?>

See also `FTP <https://www.php.net/manual/en/book.ftp.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extftp                                                                                                                                                                       |
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


