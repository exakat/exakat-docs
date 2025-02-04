.. _security-anchorregex:


.. _always-anchor-regex:

Always Anchor Regex
+++++++++++++++++++

.. meta::
	:description:
		Always Anchor Regex: Unanchored regex finds the requested pattern, and leaves room for malicious content.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Always Anchor Regex
	:twitter:description: Always Anchor Regex: Unanchored regex finds the requested pattern, and leaves room for malicious content
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Always Anchor Regex
	:og:type: article
	:og:description: Unanchored regex finds the requested pattern, and leaves room for malicious content
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Always Anchor Regex.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/AnchorRegex.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/AnchorRegex.html","name":"Always Anchor Regex","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Unanchored regex finds the requested pattern, and leaves room for malicious content","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Always Anchor Regex.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Unanchored regex finds the requested pattern, and leaves room for malicious content. 

Without ``^`` and ``$``, the regex searches for any pattern that satisfies the criteria, leaving any unused part of the string available for arbitrary content. It is recommended to use both anchor
Note that $ may be a line ending, still leaving room after it for injection.
This analysis reports `false <https://www.php.net/false>`_ positive when the regex is used to search a pattern in a much larger string. Check if this rule doesn't apply, though.

.. code-block:: php
   
   <?php
   
   $birthday = getSomeDate($_GET);
   
   // Permissive version : $birthday = '1970-01-01<script>xss();</script>';
   if (!preg_match('/\d{4}-\d{2}-\d{2}/', $birthday) {
       error('Wrong data format for your birthday!');
   }
   
   // Restrictive version : $birthday = '1970-01-01';
   if (!preg_match('/^\d{4}-\d{2}-\d{2}$/', $birthday) {
       error('Wrong data format for your birthday!');
   }
   
   echo 'Your birthday is on '.$birthday;
   
   ?>

See also `CWE-625: Permissive Regular Expression <https://cwe.mitre.org/data/definitions/625.html>`_.

Connex PHP features
-------------------

  + `Regular Expressions <https://php-dictionary.readthedocs.io/en/latest/dictionary/regex.ini.html>`_


Suggestions
___________

* Add an anchor to the beginning and ending of the string




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/AnchorRegex                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.15                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


