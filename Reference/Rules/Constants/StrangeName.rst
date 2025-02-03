.. _constants-strangename:

.. _strange-name-for-constants:

Strange Name For Constants
++++++++++++++++++++++++++

.. meta::
	:description:
		Strange Name For Constants: Those constants looks like a typo from other names.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Strange Name For Constants
	:twitter:description: Strange Name For Constants: Those constants looks like a typo from other names
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Strange Name For Constants
	:og:type: article
	:og:description: Those constants looks like a typo from other names
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Strange Name For Constants.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/StrangeName.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/StrangeName.html","name":"Strange Name For Constants","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 14 Jan 2025 12:52:58 +0000","dateModified":"Tue, 14 Jan 2025 12:52:58 +0000","description":"Those constants looks like a typo from other names","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Strange Name For Constants.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Those constants looks like a typo from other names. It is an unknown constant, and with a slight change of name, it could be another constant, that exists.

.. code-block:: php
   
   <?php
   
   // This code looks OK : DIRECTORY_SEPARATOR is a native PHP constant
   $path = $path . DIRECTORY_SEPARATOR . $file;
   
   // Strange name DIRECOTRY_SEPARATOR
   $path = $path . DIRECOTRY_SEPARATOR . $file;
   
   ?>
Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Fix any typo in the spelling of the constants
* Tell us about common misspelling so we can upgrade this analysis




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/StrangeName                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.5                                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


