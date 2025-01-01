.. _extensions-extstandard:

.. _ext-standard:

ext/standard
++++++++++++

.. meta::
	:description:
		ext/standard: Standards PHP functions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/standard
	:twitter:description: ext/standard: Standards PHP functions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/standard
	:og:type: article
	:og:description: Standards PHP functions
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extstandard.html
	:og:locale: en
Standards PHP functions.

This is not a real PHP extension : it covers the core functions.

.. code-block:: php
   
   <?php
   /*
   Our php.ini contains the following settings:
   
   display_errors = On
   register_globals = Off
   post_max_size = 8M
   */
   
   echo 'display_errors = ' . ini_get('display_errors') . PHP_EOL;
   echo 'register_globals = ' . ini_get('register_globals') . PHP_EOL;
   echo 'post_max_size = ' . ini_get('post_max_size') . PHP_EOL;
   echo 'post_max_size+1 = ' . (ini_get('post_max_size')+1) . PHP_EOL;
   echo 'post_max_size in bytes = ' . return_bytes(ini_get('post_max_size'));
   
   function return_bytes($val) {
       $val = trim($val);
       $last = strtolower($val[strlen($val)-1]);
       switch($last) {
           // The 'G' modifier is available since PHP 5.1.0
           case 'g':
               $val *= 1024;
           case 'm':
               $val *= 1024;
           case 'k':
               $val *= 1024;
       }
   
       return $val;
   }
   
   ?>

See also `PHP Options/Info Functions <https://www.php.net/manual/en/ref.info.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extstandard                                                                                                                                                                  |
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


