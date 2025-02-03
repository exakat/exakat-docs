.. _portability-linuxonlyfiles:

.. _linux-only-files:

Linux Only Files
++++++++++++++++

.. meta::
	:description:
		Linux Only Files: List of files that are only found on Linux style systems.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Linux Only Files
	:twitter:description: Linux Only Files: List of files that are only found on Linux style systems
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Linux Only Files
	:og:type: article
	:og:description: List of files that are only found on Linux style systems
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Linux Only Files.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Portability\/LinuxOnlyFiles.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Portability\/LinuxOnlyFiles.html","name":"Linux Only Files","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"List of files that are only found on Linux style systems","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Linux Only Files.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>List of files that are only found on Linux style systems. They are making the application depend on the system.

.. code-block:: php
   
   <?php
   
   // Really non-portable system check
   $os = shell_exec("cat /proc/version");
   echo "You are using $os\n";
   
   ?>
Connex PHP features
-------------------

  + `file <https://php-dictionary.readthedocs.io/en/latest/dictionary/file.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Portability/LinuxOnlyFiles                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


