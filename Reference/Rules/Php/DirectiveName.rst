.. _php-directivename:


.. _unknown-directive-name:

Unknown Directive Name
++++++++++++++++++++++

.. meta::
	:description:
		Unknown Directive Name: Unknown directives names used in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unknown Directive Name
	:twitter:description: Unknown Directive Name: Unknown directives names used in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unknown Directive Name
	:og:type: article
	:og:description: Unknown directives names used in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unknown Directive Name.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/DirectiveName.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/DirectiveName.html","name":"Unknown Directive Name","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Unknown directives names used in the code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unknown Directive Name.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Unknown directives names used in the code. 

The following list has directive mentioned in the code, that are not known from PHP or any extension. If this is due to a mistake, the directive must be fixed to be actually useful.

.. code-block:: php
   
   <?php
   
   // non-existing directive
   $reporting_error = ini_get('reporting_error');
   $error_reporting = ini_get('error_reproting'); // Note the inversion
   if (ini_set('dump_globals')) {
       // doSomething()
   }
   
   // Correct directives
   $error_reporting = ini_get('reporting_error');
   if (ini_set('xdebug.dump_globals')) {
       // doSomething()
   }
   
   ?>
Connex PHP features
-------------------

  + `Directives <https://php-dictionary.readthedocs.io/en/latest/dictionary/directive.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/DirectiveName                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


