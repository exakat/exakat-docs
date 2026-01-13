.. _extensions-extftp:

.. _ext-ftp:

ext/ftp
+++++++

  Extension FTP.

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


