.. _structures-pregoptione:

.. _preg\_replace-with-option-e:

preg_replace With Option e
++++++++++++++++++++++++++

.. meta::
	:description:
		preg_replace With Option e: preg_replace() supported the /e option until PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: preg_replace With Option e
	:twitter:description: preg_replace With Option e: preg_replace() supported the /e option until PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: preg_replace With Option e
	:og:type: article
	:og:description: preg_replace() supported the /e option until PHP 7
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/preg_replace With Option e.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/pregOptionE.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/pregOptionE.html","name":"preg_replace With Option e","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"preg_replace() supported the \/e option until PHP 7","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/preg_replace With Option e.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`preg_replace() <https://www.php.net/preg_replace>`_ supported the /e option until PHP 7.0. It allowed the use of eval()'ed expression as replacement. This has been dropped in PHP 7.0, for security reasons.

`preg_replace() <https://www.php.net/preg_replace>`_ with /e option may be replaced with `preg_replace_callback() <https://www.php.net/preg_replace_callback>`_ and a `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, or `preg_replace_callback_array() <https://www.php.net/preg_replace_callback_array>`_ and an array of closures.

.. code-block:: php
   
   <?php
   
   // preg_replace with /e
   $string = 'abcde';
   
   // PHP 5.6 and older usage of /e
   $replaced = preg_replace('/c/e', 'strtoupper($0)', $string);
   
   // PHP 7.0 and more recent
   // With one replacement
   $replaced = preg_replace_callback('/c/', function ($x) { return strtoupper($x[0]); }, $string);
   
   // With several replacements, preventing multiple calls to preg_replace_callback
   $replaced = preg_replace_callback_array(array('/c/' => function ($x) { return strtoupper($x[0]); },
                                                 '/[a-b]/' => function ($x) { return strtolower($x[0]); }), $string);
   ?>
Connex PHP features
-------------------

  + `regex <https://php-dictionary.readthedocs.io/en/latest/dictionary/regex.ini.html>`_


Suggestions
___________

* Replace call to preg_replace() and /e with preg_replace_callback() or preg_replace_callback_array()




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/pregOptionE                                                                                                                                                                                                                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>`, :ref:`Security <ruleset-Security>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-edusoho-structures-pregoptione`                                                                                                                                                                                                                                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


