.. _extensions-extzip:


.. _ext-zip:

ext/zip
+++++++

.. meta::
	:description:
		ext/zip: Extension ext/zip.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/zip
	:twitter:description: ext/zip: Extension ext/zip
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/zip
	:og:type: article
	:og:description: Extension ext/zip
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/zip.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extzip.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extzip.html","name":"ext\/zip","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension ext\/zip","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/zip.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension ext/zip.

This extension enables you to transparently read or write ZIP compressed archives and the files inside them.

.. code-block:: php
   
   <?php
   
   $zip = new ZipArchive();
   $filename = './test112.zip';
   
   if ($zip->open($filename, ZipArchive::CREATE)!==TRUE) {
       exit('cannot open <$filename>');
   }
   
   $zip->addFromString('testfilephp.txt' . time(), '#1 This is a test string added as testfilephp.txt.'.PHP_EOL);
   $zip->addFromString('testfilephp2.txt' . time(), '#2 This is a test string added as testfilephp2.txt.'.PHP_EOL);
   $zip->addFile($thisdir . '/too.php','/testfromfile.php');
   echo 'numfiles: ' . $zip->numFiles . PHP_EOL;
   echo 'status:' . $zip->status . PHP_EOL;
   $zip->close();
   ?>

See also `Zip <https://www.php.net/manual/en/book.zip.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extzip                                                                                                                                                                       |
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


