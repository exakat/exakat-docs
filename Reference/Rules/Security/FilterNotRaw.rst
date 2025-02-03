.. _security-filternotraw:


.. _filter-not-raw:

Filter Not Raw
++++++++++++++

.. meta::
	:description:
		Filter Not Raw: Report usage of filter functions with the ``FILTER_RAW_UNSAFE`` option.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Filter Not Raw
	:twitter:description: Filter Not Raw: Report usage of filter functions with the ``FILTER_RAW_UNSAFE`` option
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Filter Not Raw
	:og:type: article
	:og:description: Report usage of filter functions with the ``FILTER_RAW_UNSAFE`` option
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Filter Not Raw.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/FilterNotRaw.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/FilterNotRaw.html","name":"Filter Not Raw","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Report usage of filter functions with the ``FILTER_RAW_UNSAFE`` option","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Filter Not Raw.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Report usage of filter functions with the ``FILTER_RAW_UNSAFE`` option. This option is the default one.

.. code-block:: php
   
   <?php
   
   // default to FILTER_RAW_UNSAFE
   filter_var($a);
   
   // explicit no filter
   filter_var($a, FILTER_RAW_UNSAFE);
   
   ?>
Connex PHP features
-------------------

  + `filter <https://php-dictionary.readthedocs.io/en/latest/dictionary/filter.ini.html>`_


Suggestions
___________

* Use a different filter to validate those data.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/FilterNotRaw                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.1                                                                                                                   |
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


