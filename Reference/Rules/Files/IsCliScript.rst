.. _files-iscliscript:

.. _is-cli-script:

Is CLI Script
+++++++++++++

.. meta::
	:description:
		Is CLI Script: Mark a file as a CLI script.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Is CLI Script
	:twitter:description: Is CLI Script: Mark a file as a CLI script
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Is CLI Script
	:og:type: article
	:og:description: Mark a file as a CLI script
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Is CLI Script.html
	:og:locale: en
Mark a file as a CLI script. This means that this code is used in command line. That detection is based on the usage of distinct CLI features, such as ``#!`` at the beginning of the file.
#!/usr/bin/php

.. code-block:: php
   
   <?php
   	echo PHP_VERSION;
   ?>
Connex PHP features
-------------------

  + `cli <https://php-dictionary.readthedocs.io/en/latest/dictionary/cli.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Files/IsCliScript                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
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


