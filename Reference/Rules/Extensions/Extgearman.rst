.. _extensions-extgearman:

.. _ext-gearman:

ext/gearman
+++++++++++

.. meta::
	:description:
		ext/gearman: Extension Gearman.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/gearman
	:twitter:description: ext/gearman: Extension Gearman
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/gearman
	:og:type: article
	:og:description: Extension Gearman
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/gearman.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extgearman.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extgearman.html","name":"ext\/gearman","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension Gearman","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/gearman.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Extension Gearman.

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


