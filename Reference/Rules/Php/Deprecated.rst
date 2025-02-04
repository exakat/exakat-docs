.. _php-deprecated:


.. _deprecated-php-functions:

Deprecated PHP Functions
++++++++++++++++++++++++

.. meta::
	:description:
		Deprecated PHP Functions: The following functions are deprecated.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Deprecated PHP Functions
	:twitter:description: Deprecated PHP Functions: The following functions are deprecated
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Deprecated PHP Functions
	:og:type: article
	:og:description: The following functions are deprecated
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Deprecated PHP Functions.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Deprecated.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Deprecated.html","name":"Deprecated PHP Functions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The following functions are deprecated","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Deprecated PHP Functions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The following functions are deprecated. It is recommended to stop using them now and replace them with a durable equivalent. 

Note that these functions may be still usable : they generate warning that help tracking their usage in the log. To eradicate their usage, watch the logs, and update any deprecated warning. This way, the code won't be stuck when the function is actually removed from PHP.



.. code-block:: php
   
   <?php
   
   // This is the current function
   list($day, $month, $year) = explode('/', '08/06/1995');
   
   // This is deprecated
   list($day, $month, $year) = split('/', '08/06/1995');
   
   ?>
Connex PHP features
-------------------

  + `Cryptography <https://php-dictionary.readthedocs.io/en/latest/dictionary/crypto.ini.html>`_


Suggestions
___________

* Replace those deprecated with modern syntax
* Stop using deprecated syntax




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Deprecated                                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-deprecated <https://github.com/dseguy/clearPHP/tree/master/rules/no-deprecated.md>`__                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolphin-php-deprecated`                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


