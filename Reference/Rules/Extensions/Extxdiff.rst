.. _extensions-extxdiff:

.. _ext-xdiff:

ext/xdiff
+++++++++

.. meta::
	:description:
		ext/xdiff: Extension xdiff.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/xdiff
	:twitter:description: ext/xdiff: Extension xdiff
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/xdiff
	:og:type: article
	:og:description: Extension xdiff
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extxdiff.html
	:og:locale: en
Extension xdiff.

xdiff extension enables you to create and apply patch files containing differences between different revisions of files.

.. code-block:: php
   
   <?php
   $old_version = 'my_script-1.0.php';
   $patch = 'my_script.patch';
   
   $errors = xdiff_file_patch($old_version, $patch, 'my_script-1.1.php');
   if (is_string($errors)) {
      echo 'Rejects:'.PHP_EOL;
      echo $errors;
   }
   
   ?>

See also `libxdiff <http://www.xmailserver.org/xdiff-lib.html>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extxdiff                                                                                                                                                                     |
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


