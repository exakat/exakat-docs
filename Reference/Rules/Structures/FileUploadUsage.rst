.. _structures-fileuploadusage:

.. _file-uploads:

File Uploads
++++++++++++

.. meta\:\:
	:description:
		File Uploads: This code makes usage of file upload features of PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: File Uploads
	:twitter:description: File Uploads: This code makes usage of file upload features of PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: File Uploads
	:og:type: article
	:og:description: This code makes usage of file upload features of PHP
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/FileUploadUsage.html
	:og:locale: en
  This code makes usage of file upload features of PHP.

Upload file feature is detected through the usage of specific functions :

.. code-block:: php
   
   <?php
   $uploaddir = '/var/www/uploads/';
   $uploadfile = $uploaddir . basename($_FILES['userfile']['name']);
   
   echo '<pre>';
   if (move_uploaded_file($_FILES['userfile']['tmp_name'], $uploadfile)) {
       echo 'File is valid, and was successfully uploaded.'.PHP_EOL;
   } else {
       echo 'Possible file upload attack!'.PHP_EOL;
   }
   
   echo 'Here is some more debugging info:';
   print_r($_FILES);
   
   print '</pre>';
   
   ?>

See also `Handling file uploads <https://www.php.net/manual/en/features.file-upload.php>`_.

Connex PHP features
-------------------

  + `file-upload <https://php-dictionary.readthedocs.io/en/latest/dictionary/file-upload.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/FileUploadUsage                                                                                                                                                              |
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


