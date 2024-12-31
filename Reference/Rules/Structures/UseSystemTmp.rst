.. _structures-usesystemtmp:

.. _use-system-tmp:

Use System Tmp
++++++++++++++

.. meta\:\:
	:description:
		Use System Tmp: It is recommended to avoid hardcoding the temporary file.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use System Tmp
	:twitter:description: Use System Tmp: It is recommended to avoid hardcoding the temporary file
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use System Tmp
	:og:type: article
	:og:description: It is recommended to avoid hardcoding the temporary file
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/UseSystemTmp.html
	:og:locale: en
  It is recommended to avoid hardcoding the temporary file. It is better to rely on the system's temporary folder, which is accessible with `sys_get_temp_dir() <https://www.php.net/sys_get_temp_dir>`_.

.. code-block:: php
   
   <?php
   
   // Where the tmp is : 
   file_put_contents(sys_get_temp_dir().'/tempFile.txt', $content);
   
   
   // Avoid hard-coding tmp folder : 
   // On Linux-like systems
   file_put_contents('/tmp/tempFile.txt', $content);
   
   // On Windows systems
   file_put_contents('C:\WINDOWS\TEMP\tempFile.txt', $content);
   
   ?>

See also `PHP: When is /tmp not /tmp? <https://www.the-art-of-web.com/php/where-is-tmp/>`_.


Suggestions
___________

* Do not hardcode the temporary file, use the system's




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseSystemTmp                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


