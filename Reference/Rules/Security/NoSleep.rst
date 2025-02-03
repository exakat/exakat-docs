.. _security-nosleep:


.. _avoid-sleep()-usleep():

Avoid sleep()/usleep()
++++++++++++++++++++++

.. meta::
	:description:
		Avoid sleep()/usleep(): sleep() and usleep() help saturate the web server.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid sleep()/usleep()
	:twitter:description: Avoid sleep()/usleep(): sleep() and usleep() help saturate the web server
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid sleep()/usleep()
	:og:type: article
	:og:description: sleep() and usleep() help saturate the web server
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Avoid sleep()/usleep().html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/NoSleep.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/NoSleep.html","name":"Avoid sleep()\/usleep()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"sleep() and usleep() help saturate the web server","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Avoid sleep()\/usleep().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`sleep() <https://www.php.net/sleep>`_ and `usleep() <https://www.php.net/usleep>`_ help saturate the web server. 

Pausing the script for a specific amount of time means that the Web server is also making all related resources sleep, such as database, sockets, session, etc. This may used to set up a DOS on the server.  
As much as possible, avoid delaying the end of the script. 

`sleep() <https://www.php.net/sleep>`_ and `usleep() <https://www.php.net/usleep>`_ have less impact in commandline (``CLI``).

.. code-block:: php
   
   <?php
   
   $begin = microtime(true);
   checkLogin($user, $password);
   $end   = microtime(true);
   
   // Making all login checks looks the same
   usleep(1000000 - ($end - $begin) * 1000000); 
   
   // Any hit on this page now uses 1 second, no matter if load is high or not
   // Is it now possible to saturate the webserver in 1 s ? 
   
   ?>
Connex PHP features
-------------------

  + `sleep <https://php-dictionary.readthedocs.io/en/latest/dictionary/sleep.ini.html>`_
  + `cli <https://php-dictionary.readthedocs.io/en/latest/dictionary/cli.ini.html>`_


Suggestions
___________

* Add a deadline of usage in the session, and wait past this deadline to start serving again. Until then, abort immediately.
* Use element in the GUI to delay or slow usage.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/NoSleep                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


