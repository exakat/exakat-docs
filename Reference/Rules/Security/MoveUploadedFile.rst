.. _security-moveuploadedfile:


.. _move\_uploaded\_file-instead-of-copy:

move_uploaded_file Instead Of copy
++++++++++++++++++++++++++++++++++


.. meta::

	:description:

		move_uploaded_file Instead Of copy: Always use move_uploaded_file() with uploaded files.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: move_uploaded_file Instead Of copy

	:twitter:description: move_uploaded_file Instead Of copy: Always use move_uploaded_file() with uploaded files

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: move_uploaded_file Instead Of copy

	:og:type: article

	:og:description: Always use move_uploaded_file() with uploaded files

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/move_uploaded_file Instead Of copy.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/MoveUploadedFile.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/MoveUploadedFile.html","name":"move_uploaded_file Instead Of copy","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Always use move_uploaded_file() with uploaded files","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/move_uploaded_file Instead Of copy.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Always use `move_uploaded_file() <https://www.php.net/move_uploaded_file>`_ with uploaded files. Avoid using copy or rename with uploaded file. 

`move_uploaded_file() <https://www.php.net/move_uploaded_file>`_ checks to ensure that the file designated by filename is a valid upload file (meaning that it was uploaded via PHP's HTTP POST upload mechanism).

.. code-block:: php
   
   <?php
   
       // $a->file was filled with $_FILES at some point
       move_uploaded_file($a->file['tmp_name'], $target);
   
       // $a->file was filled with $_FILES at some point
       rename($a->file['tmp_name'], $target);
   
   ?>

See also `move_uploaded_file <https://www.php.net/move_uploaded_file>`_ and `Uploading Files with PHP <https://www.sitepoint.com/file-uploads-with-php/>`_.

Connex PHP features
-------------------

  + `file-upload <https://php-dictionary.readthedocs.io/en/latest/dictionary/file-upload.ini.html>`_


Suggestions
___________

* Always use move_uploaded_file() 
* Extract the needed information from the file, and leave it for PHP to remove without storage




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/MoveUploadedFile                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


