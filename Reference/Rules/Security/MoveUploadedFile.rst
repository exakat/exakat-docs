.. _security-moveuploadedfile:

.. _move\_uploaded\_file-instead-of-copy:

move_uploaded_file Instead Of copy
++++++++++++++++++++++++++++++++++

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


