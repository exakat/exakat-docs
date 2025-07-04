.. _php-phperrormsgusage:


.. _$php\_errormsg-usage:

$php_errormsg Usage
+++++++++++++++++++

.. meta::
	:description:
		$php_errormsg Usage: The variable $php_errormsg is removed since PHP 8.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: $php_errormsg Usage
	:twitter:description: $php_errormsg Usage: The variable $php_errormsg is removed since PHP 8
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: $php_errormsg Usage
	:og:type: article
	:og:description: The variable $php_errormsg is removed since PHP 8
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/$php_errormsg Usage.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/PhpErrorMsgUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/PhpErrorMsgUsage.html","name":"$php_errormsg Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"The variable $php_errormsg is removed since PHP 8","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/$php_errormsg Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The variable $php_errormsg is removed since PHP 8.0. $php_errormsg tracks the last `error <https://www.php.net/error>`_ message, with the directive `track_errors`. All was removed in PHP 8.0, and shall be replaced with `error_get_last() <https://www.php.net/error_get_last>`_.

.. code-block:: php
   
   <?php
   
   function foo() {
       global $php_errormsg;
       
       echo 'Last error: '.$php_errormsg;
       
       echo 'Also, last error: '.error_get_last();
   }
   
   ?>
Connex PHP features
-------------------

  + `$php_errormsg <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24php_errormsg.ini.html>`_


Suggestions
___________

* Use error_get_last() instead.




Specs
_____

+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/PhpErrorMsgUsage                                                                                                                                                                    |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`                            |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.1.8                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 8.0 and older                                                                                                                                                                  |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/php_errormsg.html>`__                                                                                  |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | High                                                                                                                                                                                    |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


