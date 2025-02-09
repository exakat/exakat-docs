.. _structures-unknownpregoption:


.. _unkown-regex-options:

Unkown Regex Options
++++++++++++++++++++

.. meta::
	:description:
		Unkown Regex Options: Regex support in PHP accepts the following list of options : ``eimsuxADJSUX``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unkown Regex Options
	:twitter:description: Unkown Regex Options: Regex support in PHP accepts the following list of options : ``eimsuxADJSUX``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unkown Regex Options
	:og:type: article
	:og:description: Regex support in PHP accepts the following list of options : ``eimsuxADJSUX``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unkown Regex Options.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UnknownPregOption.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UnknownPregOption.html","name":"Unkown Regex Options","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Regex support in PHP accepts the following list of options : ``eimsuxADJSUX``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unkown Regex Options.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Regex support in PHP accepts the following list of options : ``eimsuxADJSUX``. 

All other letter used as option are not supported : depending on the situation, they may be ignored or raise an `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   // all options are available
   if (preg_match('/\d+/isA', $string, $results)) { }
   
   // p and h are not regex options, p is double
   if (preg_match('/\d+/php', $string, $results)) { }
   
   ?>

See also `Pattern Modifiers <https://www.php.net/manual/en/reference.pcre.pattern.modifiers.php>`_.

Connex PHP features
-------------------

  + `Regular Expressions <https://php-dictionary.readthedocs.io/en/latest/dictionary/regex.ini.html>`_


Suggestions
___________

* Remove the unknown options
* Replace the option with a valid one
* Fix any syntax typo in the regex




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UnknownPregOption                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


