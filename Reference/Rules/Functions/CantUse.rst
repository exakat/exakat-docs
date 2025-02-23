.. _functions-cantuse:


.. _methods-that-should-not-be-used:

Methods That Should Not Be Used
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		Methods That Should Not Be Used: These methods and functions only throw an exception, or raise an error.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Methods That Should Not Be Used
	:twitter:description: Methods That Should Not Be Used: These methods and functions only throw an exception, or raise an error
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Methods That Should Not Be Used
	:og:type: article
	:og:description: These methods and functions only throw an exception, or raise an error
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Methods That Should Not Be Used.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/CantUse.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/CantUse.html","name":"Methods That Should Not Be Used","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"These methods and functions only throw an exception, or raise an error","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Methods That Should Not Be Used.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

These methods and functions only throw an `exception <https://www.php.net/exception>`_, or raise an `error <https://www.php.net/error>`_. As such, they are a warning that such function or method shouldn't be used. 
Those functions could also be marked as deprecated, with an `attribute <https://www.php.net/attribute>`_ or a phpdoc. This is not taken into account by this analysis.

.. code-block:: php
   
   <?php
   
   function obsoleteFoo() {
       throw new exception('Don\'t use obsoleteFoo() but rather the new version of foo().');
   }
   ?>
Connex PHP features
-------------------

  + `Functions <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `Deprecated <https://php-dictionary.readthedocs.io/en/latest/dictionary/deprecated.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/CantUse                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.7                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


