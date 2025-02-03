.. _structures-resourcesusage:

.. _resources-usage:

Resources Usage
+++++++++++++++

.. meta::
	:description:
		Resources Usage: List of instructions that are creating resources.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Resources Usage
	:twitter:description: Resources Usage: List of instructions that are creating resources
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Resources Usage
	:og:type: article
	:og:description: List of instructions that are creating resources
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Resources Usage.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ResourcesUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ResourcesUsage.html","name":"Resources Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 28 Jan 2025 15:14:39 +0000","dateModified":"Tue, 28 Jan 2025 15:14:39 +0000","description":"List of instructions that are creating resources","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Resources Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>List of instructions that are creating resources. Resources are a ancient PHP datastructure, which is gradually being deprecated. Resources were often created by PHP extensions, as the first step of their usage. They are now converted into objects.

For example, ``fopen()`` produces a ``resource``. ``finfo_open`` used to return a ``resource`` until PHP 8.1, and now, returns an object.

.. code-block:: php
   
   <?php
   
   // This functioncall creates a resource to use
   $fp = fopen('/tmp/file.txt', 'r');
   
   if (!is_resource($fp)){
       thrown new RuntimeException('Could not open file.txt');
   }
   
   ?>
Connex PHP features
-------------------

  + `resource <https://php-dictionary.readthedocs.io/en/latest/dictionary/resource.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ResourcesUsage                                                                                                                                                               |
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


