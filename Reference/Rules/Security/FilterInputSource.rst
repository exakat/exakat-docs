.. _security-filterinputsource:

.. _filter\_input()-as-a-source:

filter_input() As A Source
++++++++++++++++++++++++++

.. meta::
	:description:
		filter_input() As A Source: The filter_input() and filter_input_array() functions access directly to ``$_GET``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: filter_input() As A Source
	:twitter:description: filter_input() As A Source: The filter_input() and filter_input_array() functions access directly to ``$_GET``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: filter_input() As A Source
	:og:type: article
	:og:description: The filter_input() and filter_input_array() functions access directly to ``$_GET``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/filter_input() As A Source.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/FilterInputSource.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/FilterInputSource.html","name":"filter_input() As A Source","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The filter_input() and filter_input_array() functions access directly to ``$_GET``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/filter_input() As A Source.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The `filter_input() <https://www.php.net/filter_input>`_ and `filter_input_array() <https://www.php.net/filter_input_array>`_ functions access directly to ``$_GET``. They represent a source for external data just like ``$_GET``, ``$_POST``, etc.

The main feature of `filter_input() <https://www.php.net/filter_input>`_ is that it is already filtered. The main drawback is that ``FILTER_FLAG_NONE`` is the ``none`` filter, and that default configuration is `FILTER_UNSAFE_RAW`.

The filter extension keeps access to the incoming data, even after the super globals, such as ``$_GET``, are unset.
Thanks to `Frederic Bouchery <https://twitter.com/FredBouchery/>`_ for reporting this `special case <https://twitter.com/FredBouchery/status/1049297213598457857>`_.

.. code-block:: php
   
   <?php
   
   // Removing $_GET
   $_GET = [];
   
   // with the default : FILTER_UNSAFE_RAW, this means XSS
   echo filter_input(INPUT_GET, 'i');
   
   // Same as above : 
   echo filter_var(_GET, 'i');
   
   ?>

See also `Data filtering <https://www.php.net/manual/en/book.filter.php>`_.

Connex PHP features
-------------------

  + `validation <https://php-dictionary.readthedocs.io/en/latest/dictionary/validation.ini.html>`_


Suggestions
___________

* Use the classic $_GET, $_POST super globals, which are easier to audit.
* Use your framework's parameter access.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/FilterInputSource                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


