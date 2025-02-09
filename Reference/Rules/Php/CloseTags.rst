.. _php-closetags:


.. _closing-tags:

Closing Tags
++++++++++++

.. meta::
	:description:
		Closing Tags: PHP manual recommends that script should be left open, without the final closing ``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Closing Tags
	:twitter:description: Closing Tags: PHP manual recommends that script should be left open, without the final closing ``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Closing Tags
	:og:type: article
	:og:description: PHP manual recommends that script should be left open, without the final closing ``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Closing Tags.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CloseTags.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CloseTags.html","name":"Closing Tags","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP manual recommends that script should be left open, without the final closing ``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Closing Tags.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP manual recommends that script should be left open, without the final closing ``?>``. This way, one will avoid the infamous bug ``'Header already sent'``, associated with left-over spaces, that are lying after this closing tag.
<?php

// some code

// no closing tag

See also `PHP Closing Tag <https://codeigniter.com/userguide3/general/styleguide.html#php-closing-tag>`_.

Connex PHP features
-------------------

  + `Close Tag <https://php-dictionary.readthedocs.io/en/latest/dictionary/close-tag.ini.html>`_


Suggestions
___________

* Always leave the last closing tag out




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CloseTags                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Coding conventions <ruleset-Coding-conventions>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `leave-last-closing-out <https://github.com/dseguy/clearPHP/tree/master/rules/leave-last-closing-out.md>`__             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


