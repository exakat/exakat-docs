.. _php-usestrcontains:

.. _use-str\_contains():

Use str_contains()
++++++++++++++++++

.. meta::
	:description:
		Use str_contains(): str_contains() checks if a string is within another one.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use str_contains()
	:twitter:description: Use str_contains(): str_contains() checks if a string is within another one
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use str_contains()
	:og:type: article
	:og:description: str_contains() checks if a string is within another one
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use str_contains().html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseStrContains.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseStrContains.html","name":"Use str_contains()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"str_contains() checks if a string is within another one","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use str_contains().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`str_contains() <https://www.php.net/str_contains>`_ checks if a string is within another one. It replaces a call to `strpos() <https://www.php.net/strpos>`_ with a comparison. 
Note that this function is case sensitive : it cannot replace `stripos() <https://www.php.net/stripos>`_.

Note that this function is single-byte only : it cannot replace `mb_strpos() <https://www.php.net/mb_strpos>`_.

This analysis omits calls to `strpos() <https://www.php.net/strpos>`_ that are saved to a variable. `strpos() <https://www.php.net/strpos>`_ is actually returning the position of the found string in the haystack, which may be reused later.

.. code-block:: php
   
   <?php
    
   if (str_contains("abc", "a")) { doSomething(); }
   
   // strpos is used only for detection.
   if (strpos("abc", "a") !== false) { doSomething(); }
   
   // strpos returns a position, 
   $pos = strpos("abca", "a", 3);
   if ($pos > 3) { doSomething();
   
   ?>

See also `PHP RFC: str_contains <https://wiki.php.net/rfc/str_contains>`_.

Connex PHP features
-------------------

  + `string <https://php-dictionary.readthedocs.io/en/latest/dictionary/string.ini.html>`_


Suggestions
___________

* Switch to str_contains()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseStrContains                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


