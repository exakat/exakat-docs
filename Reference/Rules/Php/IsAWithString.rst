.. _php-isawithstring:

.. _is\_a()-with-string:

Is_A() With String
++++++++++++++++++

.. meta::
	:description:
		Is_A() With String: When using is_a() with a string as first argument, the third argument is compulsory.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Is_A() With String
	:twitter:description: Is_A() With String: When using is_a() with a string as first argument, the third argument is compulsory
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Is_A() With String
	:og:type: article
	:og:description: When using is_a() with a string as first argument, the third argument is compulsory
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Is_A() With String.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/IsAWithString.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/IsAWithString.html","name":"Is_A() With String","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When using is_a() with a string as first argument, the third argument is compulsory","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Is_A() With String.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>When using `is_a() <https://www.php.net/is_a>`_ with a string as first argument, the third argument is compulsory. The third argument is ``$allow_string``, and is necessary to work on strings.

.. code-block:: php
   
   <?php
   
   // is_a() works with string as first argument, when the third argument is 'true'
   if (is_a('A', 'B', true)) {}
   
   // is_a() works with object as first argument
   if (is_a(new A, 'A')) {}
   ?>

See also `is_a <https://www.php.net/is_a>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Suggestions
___________

* Add the third argument, and set it to true
* Use an object as a first argument




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/IsAWithString                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Rector <ruleset-Rector>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


