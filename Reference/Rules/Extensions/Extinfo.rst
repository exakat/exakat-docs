.. _extensions-extinfo:

.. _ext-info:

ext/info
++++++++

  PHP Options and Information.

These functions enable you to get a lot of information about PHP itself, e.g. runtime configuration, loaded extensions, version and much more. 


.. code-block:: php
   
   <?php
   /*
   Our php.ini contains the following settings:
   
   display_errors = On
   register_globals = Off
   post_max_size = 8M
   */
   
   echo 'display_errors = ' . ini_get('display_errors') . "\n";
   echo 'register_globals = ' . ini_get('register_globals') . "\n";
   echo 'post_max_size = ' . ini_get('post_max_size') . "\n";
   echo 'post_max_size+1 = ' . (ini_get('post_max_size')+1) . "\n";
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

See also `PHP Options And Information <https://www.php.net/manual/en/book.info.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extinfo                                                                                                                                                                      |
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


