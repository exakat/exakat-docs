.. _files-notdefinitionsonly:


.. _file-is-not-definitions-only:

File Is Not Definitions Only
++++++++++++++++++++++++++++


.. meta::

	:description:

		File Is Not Definitions Only: An included file should only provide definitions and declarations, or executable code : not both.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: File Is Not Definitions Only

	:twitter:description: File Is Not Definitions Only: An included file should only provide definitions and declarations, or executable code : not both

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: File Is Not Definitions Only

	:og:type: article

	:og:description: An included file should only provide definitions and declarations, or executable code : not both

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/File Is Not Definitions Only.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Files\/NotDefinitionsOnly.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Files\/NotDefinitionsOnly.html","name":"File Is Not Definitions Only","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"An included file should only provide definitions and declarations, or executable code : not both","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/File Is Not Definitions Only.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

An included file should only provide definitions and declarations, or executable code : not both. 

With definitions only files, their inclusion provide new features, and keep the current execution untouched, and in control of the flow.
Within this context, globals, use, and namespaces instructions are not considered a warning.

.. code-block:: php
   
   <?php
   // This whole script is a file
   
   // It contains definitions and global code
   class foo {
       static public $foo = null;
   }
   //This can be a singleton creation
   foo::$foo = new foo();
   
   trait t {}
   
   class bar {}
   
   ?>

Suggestions
___________

* Remove the executable code from the file
* Remove the definitions from the file




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Files/NotDefinitionsOnly                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


