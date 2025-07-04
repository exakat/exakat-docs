.. _security-uploadfilenameinjection:


.. _upload-filename-injection:

Upload Filename Injection
+++++++++++++++++++++++++

.. meta::
	:description:
		Upload Filename Injection: When receiving a file via Upload, it is recommended to store it under a self-generated name.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Upload Filename Injection
	:twitter:description: Upload Filename Injection: When receiving a file via Upload, it is recommended to store it under a self-generated name
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Upload Filename Injection
	:og:type: article
	:og:description: When receiving a file via Upload, it is recommended to store it under a self-generated name
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Upload Filename Injection.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/UploadFilenameInjection.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/UploadFilenameInjection.html","name":"Upload Filename Injection","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When receiving a file via Upload, it is recommended to store it under a self-generated name","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Upload Filename Injection.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When receiving a file via Upload, it is recommended to store it under a `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_-generated name. Any storage that uses the original filename, or even a part of it may be vulnerable to injections.
It is highly recommended to validate any incoming file, generate a name for it, and store the `result <https://www.php.net/result>`_ in a folder outside the web folder. Also, avoid accepting PHP scripts, if possible.

.. code-block:: php
   
   <?php
   
   // Security error ! the $_FILES['upload']['filename'] is provided by the sender.
   // 'a.<script>alert(\'a\')</script>'; may lead to a HTML injection.
   $extension = substr( strrchr($_FILES['upload']['name'], '.') ,1);
   if (!in_array($extension, array('gif', 'jpeg', 'jpg')) { 
       // process error
       continue;
   }
   // Md5 provides a name without special characters
   $name = md5($_FILES['upload']['filename']);
   if(@move_uploaded_file($_FILES['upload']['tmp_name'], '/var/no-www/upload/'.$name.'.'.$extension)) {
       safeStoring($name.'.'.$extension, $_FILES['upload']['filename']);
   }
   
   // Security error ! the $_FILES['upload']['filename'] is provided by the sender.
   if(@move_uploaded_file($_FILES['upload']['tmp_name'], $_FILES['upload']['filename'])) {
       safeStoring($_FILES['upload']['filename']);
   }
   
   // Security error ! the $_FILES['upload']['filename'] is provided by the sender.
   // 'a.<script>alert('a')</script>'; may lead to a HTML injection.
   $extension = substr( strrchr($_FILES['upload']['name'], '.') ,1);
   $name = md5($_FILES['upload']['filename']);
   if(@move_uploaded_file($_FILES['upload']['tmp_name'], $name.'.'.$extension)) {
       safeStoring($name.'.'.$extension, $_FILES['upload']['filename']);
   }
   
   ?>

See also `[CVE-2017-6090] <https://cxsecurity.com/issue/WLB-2017100031>`_, `CWE-616: Incomplete Identification of Uploaded File Variables <https://cwe.mitre.org/data/definitions/616.html>`_ and `Why File Upload Forms are a Major Security Threat <https://www.acunetix.com/websitesecurity/upload-forms-threat/>`_.

Connex PHP features
-------------------

  + `File Upload <https://php-dictionary.readthedocs.io/en/latest/dictionary/upload.ini.html>`_


Suggestions
___________

* Validate uploaded filenames
* Rename files upon storage, and keep the original name in a database




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/UploadFilenameInjection                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.14                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


