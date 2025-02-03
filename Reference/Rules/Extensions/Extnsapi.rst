.. _extensions-extnsapi:

.. _ext-nsapi:

ext/nsapi
+++++++++

.. meta::
	:description:
		ext/nsapi: NSAPI specific functions calls.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/nsapi
	:twitter:description: ext/nsapi: NSAPI specific functions calls
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/nsapi
	:og:type: article
	:og:description: NSAPI specific functions calls
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/nsapi.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extnsapi.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extnsapi.html","name":"ext\/nsapi","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"NSAPI specific functions calls","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/nsapi.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>NSAPI specific functions calls. 

These functions are only available when running PHP as a NSAPI module in Netscape/iPlanet/Sun webservers.

.. code-block:: php
   
   <?php
   
   // This scripts depends on ext/nsapi
   if (ini_get('nsapi.read_timeout') < 60) {
       doSomething();
   }
   
   ?>

See also `Sun, iPlanet and Netscape servers on Sun Solaris <https://www.php.net/manual/en/install.unix.sun.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extnsapi                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.2                                                                                                                                                                                   |
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


