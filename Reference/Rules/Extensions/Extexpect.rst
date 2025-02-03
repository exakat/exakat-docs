.. _extensions-extexpect:


.. _ext-expect:

ext/expect
++++++++++

.. meta::
	:description:
		ext/expect: Extension Expect.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/expect
	:twitter:description: ext/expect: Extension Expect
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/expect
	:og:type: article
	:og:description: Extension Expect
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/expect.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extexpect.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extexpect.html","name":"ext\/expect","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension Expect","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/expect.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension Expect.

This extension allows to interact with processes through ``PTY``. You may consider using the ``expect://`` wrapper with the filesystem functions which provide a simpler and more intuitive interface.

.. code-block:: php
   
   <?php
   ini_set('expect.loguser', 'Off');
   
   $stream = fopen('expect://ssh root@remotehost uptime', 'r');
   
   $cases = array (
       array (0 => 'password:', 1 => PASSWORD)
   );
   
   switch (expect_expectl ($stream, $cases)) {
       case PASSWORD:
           fwrite ($stream, 'password'.PHP_EOL);
           break;
    
       default:
           die ('Error was occurred while connecting to the remote host!'.PHP_EOL);
   }
   
   while ($line = fgets($stream)) {
         print $line;
   }
   fclose ($stream);
   ?>

See also `expect <https://www.php.net/manual/en/book.expect.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extexpect                                                                                                                                                                    |
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


