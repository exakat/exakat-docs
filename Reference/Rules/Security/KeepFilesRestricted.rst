.. _security-keepfilesrestricted:


.. _keep-files-access-restricted:

Keep Files Access Restricted
++++++++++++++++++++++++++++

.. meta::
	:description:
		Keep Files Access Restricted: Avoid using 0777 as file or directory mode.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Keep Files Access Restricted
	:twitter:description: Keep Files Access Restricted: Avoid using 0777 as file or directory mode
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Keep Files Access Restricted
	:og:type: article
	:og:description: Avoid using 0777 as file or directory mode
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Keep Files Access Restricted.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/KeepFilesRestricted.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/KeepFilesRestricted.html","name":"Keep Files Access Restricted","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"Avoid using 0777 as file or directory mode","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Keep Files Access Restricted.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid using 0777 as file or `directory <https://www.php.net/`directory <https://www.php.net/directory>`_>`_ mode. In particular, setting a file or a `directory <https://www.php.net/`directory <https://www.php.net/directory>`_>`_ to 0777 (or universal read-write-execute) may lead to security vulnerabilities, as anything on the server may read, write and even execute

File mode may be changed using the `chmod() <https://www.php.net/chmod>`_ function, or at `directory <https://www.php.net/`directory <https://www.php.net/directory>`_>`_ creation, with `mkdir() <https://www.php.net/mkdir>`_.
By default, this analysis report universal access (0777). It is possible to make this analysis more restrictive, by providing more forbidden modes in the ``filePrivileges`` parameter. For example : ``511,510,489``. Only use a decimal representation.

.. code-block:: php
   
   <?php
   
   file_put_contents($file, $content);
   
   // this file is accessible to the current user, and to his group, for reading and writing. 
   chmod($file, 0550); 
   
   // this file is accessible to everyone 
   chmod($file, 0777); 
   
   ?>

+----------------+---------+--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Name           | Default | Type   | Description                                                                                                                                                  |
+----------------+---------+--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| filePrivileges | 0777    | string | List of forbidden file modes (comma separated). This should be a decimal value : 511 instead of 777. The values will not be converted from octal to decimal. |
+----------------+---------+--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+



See also :ref:`Mkdir Default <mkdir-default>` and `Least Privilege Violation <https://owasp.org/www-community/vulnerabilities/Least_Privilege_Violation>`_.

Connex PHP features
-------------------

  + `file-access <https://php-dictionary.readthedocs.io/en/latest/dictionary/file-access.ini.html>`_


Suggestions
___________

* Set the file mode to a level of restriction as low as possible.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/KeepFilesRestricted                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


