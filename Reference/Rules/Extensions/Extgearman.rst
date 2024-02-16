.. _extensions-extgearman:

.. _ext-gearman:

ext/gearman
+++++++++++

  Extension Gearman.

Gearman is a generic application framework for farming out work to multiple machines or processes. 


.. code-block:: php
   
   <?php
   
   # Create our client object.
   $gmclient= new GearmanClient();
   
   # Add default server (localhost).
   $gmclient->addServer();
   
   echo 'Sending job'.PHP_EOL;
   
   # Send reverse job
   do
   {
     $result = $gmclient->doNormal('reverse', 'Hello!');
   
     # Check for various return packets and errors.
     switch($gmclient->returnCode())
     {
       case GEARMAN_WORK_DATA:
         echo 'Data: '.$result . PHP_EOL;;
         break;
       case GEARMAN_WORK_STATUS:
         list($numerator, $denominator)= $gmclient->doStatus();
         echo 'Status: '.$numerator.'/'.$denominator.' complete'. PHP_EOL;
         break;
       case GEARMAN_WORK_FAIL:
         echo 'Failed\n';
         exit;
       case GEARMAN_SUCCESS:
         echo 'Success: $result\n';
         break;
       default:
         echo 'RET: ' . $gmclient->returnCode() . PHP_EOL;
         exit;
     }
   }
   while($gmclient->returnCode() != GEARMAN_SUCCESS);
   
   ?>

See also `Gearman on PHP <https://www.php.net/manual/en/book.gearman.php>`_ and `Gearman <http://gearman.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extgearman                                                                                                                                                                   |
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


