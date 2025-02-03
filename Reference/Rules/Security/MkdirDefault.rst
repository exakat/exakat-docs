.. _security-mkdirdefault:

.. _mkdir-default:

Mkdir Default
+++++++++++++

.. meta::
	:description:
		Mkdir Default: mkdir() gives universal access to created folders, by default.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mkdir Default
	:twitter:description: Mkdir Default: mkdir() gives universal access to created folders, by default
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mkdir Default
	:og:type: article
	:og:description: mkdir() gives universal access to created folders, by default
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mkdir Default.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/MkdirDefault.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/MkdirDefault.html","name":"Mkdir Default","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"mkdir() gives universal access to created folders, by default","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Mkdir Default.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`mkdir() <https://www.php.net/mkdir>`_ gives universal access to created folders, by default. It is recommended to gives limited set of rights (0755, 0700), or to explicitly set the rights to 0777.

.. code-block:: php
   
   <?php
   
   // By default, this dir is 777
   mkdir('/path/to/dir');
   
   // Explicitely, this is wanted. It may also be audited easily
   mkdir('/path/to/dir', 0777);
   
   // This dir is limited to the current user. 
   mkdir('/path/to/dir', 0700);
   
   ?>

See also `Why 777 Folder Permissions are a Security Risk <https://www.spiralscripts.co.uk/Blog/why-777-folder-permissions-are-a-security-risk.html>`_.

Connex PHP features
-------------------

  + `dir <https://php-dictionary.readthedocs.io/en/latest/dictionary/dir.ini.html>`_


Suggestions
___________

* Always use the lowest possible privileges on folders
* Don't use the PHP default : at least, make it explicit that the 'universal' rights are voluntary




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/MkdirDefault                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.2                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-mautic-security-mkdirdefault`, :ref:`case-openemr-security-mkdirdefault`                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


