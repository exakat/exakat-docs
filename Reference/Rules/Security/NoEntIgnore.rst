.. _security-noentignore:


.. _no-ent\_ignore:

No ENT_IGNORE
+++++++++++++

.. meta::
	:description:
		No ENT_IGNORE: Certain characters have special significance in HTML, and should be represented by HTML entities if they are to preserve their meanings.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No ENT_IGNORE
	:twitter:description: No ENT_IGNORE: Certain characters have special significance in HTML, and should be represented by HTML entities if they are to preserve their meanings
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No ENT_IGNORE
	:og:type: article
	:og:description: Certain characters have special significance in HTML, and should be represented by HTML entities if they are to preserve their meanings
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No ENT_IGNORE.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/NoEntIgnore.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/NoEntIgnore.html","name":"No ENT_IGNORE","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Certain characters have special significance in HTML, and should be represented by HTML entities if they are to preserve their meanings","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No ENT_IGNORE.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Certain characters have special significance in HTML, and should be represented by HTML entities if they are to preserve their meanings.

`ENT_IGNORE <https://www.php.net/ent_ignore>`_ is a configuration option for `htmlspecialchars() <https://www.php.net/htmlspecialchars>`_, that ignore any needed character replacement. This mean the raw input will now be processed by PHP, or a target browser.

It is recommended to use the other configuration options : ``ENT_COMPAT``, ``ENT_QUOTES``, ``ENT_NOQUOTES``, ``ENT_SUBSTITUTE``, ``ENT_DISALLOWED``, ``ENT_HTML401``, ``ENT_XML1``, ``ENT_XHTML`` or ``ENT_HTML5``.

.. code-block:: php
   
   <?php
   
   // This produces a valid HTML tag
   $new = htmlspecialchars("<a href='test'>Test</a>", ENT_IGNORE);
   echo $new; // &lt;a href=&#039;test&#039;&gt;Test&lt;/a&gt;
   
   // This produces a valid string, without any HTML special value
   $new = htmlspecialchars("<a href='test'>Test</a>", ENT_QUOTES);
   echo $new; // &lt;a href=&#039;test&#039;&gt;Test&lt;/a&gt;
   
   ?>

See also `htmlspecialchars <https://www.php.net/htmlspecialchars>`_ and `Deletion of Code Points <http://unicode.org/reports/tr36/#Deletion_of_Noncharacters>`_.

Connex PHP features
-------------------

  + `HTML Escaping <https://php-dictionary.readthedocs.io/en/latest/dictionary/html-escape.ini.html>`_


Suggestions
___________

* Use of the the other options




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/NoEntIgnore                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                   |
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


