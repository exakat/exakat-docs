.. _constants-inconsistantcase:

.. _true-false-inconsistant-case:

True False Inconsistant Case
++++++++++++++++++++++++++++

.. meta::
	:description:
		True False Inconsistant Case: TRUE, true or True is the favorite way to write these values.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: True False Inconsistant Case
	:twitter:description: True False Inconsistant Case: TRUE, true or True is the favorite way to write these values
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: True False Inconsistant Case
	:og:type: article
	:og:description: TRUE, true or True is the favorite way to write these values
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/True False Inconsistant Case.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/InconsistantCase.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/InconsistantCase.html","name":"True False Inconsistant Case","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"TRUE, true or True is the favorite way to write these values","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/True False Inconsistant Case.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`TRUE <https://www.php.net/TRUE>`_, true or True is the favorite way to write these values.

Usually, source code chooses either ALL CAPS booleans and null, either all lowercase. Sometimes, there is no standard.

When the source code uses a majority of one of the above convention, then the analyzer reports all remaining inconsistently cased constants.

This rule works on booleans and the null value, altogether.


.. code-block:: php
   
   <?php
   
   $a1 = true;
   $a2 = true;
   $a3 = true;
   $a4 = true;
   $a5 = true;
   $a6 = true;
   $a7 = true;
   $a8 = true;
   $a9 = true;
   $a10 = true;
   
   // This convention is inconsistence with the rest
   $b1 = TRUE;
   ?>

See also `PHP Constants <https://www.php.net/manual/en/language.constants.php>`_.

Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/InconsistantCase                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
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


