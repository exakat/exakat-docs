.. _structures-uncheckedresources:


.. _unchecked-resources:

Unchecked Resources
+++++++++++++++++++

.. meta::
	:description:
		Unchecked Resources: Resources are created, but never checked before being used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unchecked Resources
	:twitter:description: Unchecked Resources: Resources are created, but never checked before being used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unchecked Resources
	:og:type: article
	:og:description: Resources are created, but never checked before being used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unchecked Resources.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UncheckedResources.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UncheckedResources.html","name":"Unchecked Resources","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Resources are created, but never checked before being used","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unchecked Resources.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Resources are created, but never checked before being used. This is not safe.

Always check that resources are correctly created before using them.

.. code-block:: php
   
   <?php
   
   // always check that the resource is created correctly
   $fp = fopen($d,'r');
   if ($fp === false) {
       throw new Exception('File not found');
   } 
   $firstLine = fread($fp);
   
   // This directory is not checked : the path may not exist and return false
   $uncheckedDir = opendir($pathToDir);
   while(readdir($uncheckedDir)) {
       // do something()
   }
   
   // This file is not checked : the path may not exist or be unreadable and return false
   $fp = fopen($pathToFile);
   while($line = freads($fp)) {
       $text .= $line;
   }
   
   // unsafe one-liner : using bzclose on an unchecked resource
   bzclose(bzopen('file'));
   
   ?>

See also `resources <https://www.php.net/manual/en/language.types.resource.php>`_.

Connex PHP features
-------------------

  + `resource <https://php-dictionary.readthedocs.io/en/latest/dictionary/resource.ini.html>`_


Suggestions
___________

* Add a check between the resource acquisition and its usage




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UncheckedResources                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-unchecked-resources <https://github.com/dseguy/clearPHP/tree/master/rules/no-unchecked-resources.md>`__                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


