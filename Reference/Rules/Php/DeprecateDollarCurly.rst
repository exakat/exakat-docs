.. _php-deprecatedollarcurly:


.. _dollar-curly-interpolation-is-deprecated:

Dollar Curly Interpolation Is Deprecated
++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Dollar Curly Interpolation Is Deprecated: Among the different variable interpolation is strings, ```` is deprecated.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dollar Curly Interpolation Is Deprecated
	:twitter:description: Dollar Curly Interpolation Is Deprecated: Among the different variable interpolation is strings, ```` is deprecated
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dollar Curly Interpolation Is Deprecated
	:og:type: article
	:og:description: Among the different variable interpolation is strings, ```` is deprecated
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dollar Curly Interpolation Is Deprecated.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/DeprecateDollarCurly.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/DeprecateDollarCurly.html","name":"Dollar Curly Interpolation Is Deprecated","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Among the different variable interpolation is strings, ```` is deprecated","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Dollar Curly Interpolation Is Deprecated.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Among the different variable interpolation is strings, ```` is deprecated. It is made obsolete in PHP 8.2, and should disappear in PHP 9.0.

There are still several interpolation ways : variables, array elements (one index-level) and curly brackets. It is also possible to use string concatenation.

.. code-block:: php
   
   <?php
   
   $a = 'a';
   $a2 = 'surprise!';
   
   $b = "\$\{$a . 2}"; 
   
   echo $b;
   // display 'surprise!'
   
   ?>

See also https://wiki.php.net/rfc/deprecate_dollar_brace_string_interpolation.

Connex PHP features
-------------------

  + `string <https://php-dictionary.readthedocs.io/en/latest/dictionary/string.ini.html>`_
  + `string-interpolation <https://php-dictionary.readthedocs.io/en/latest/dictionary/string-interpolation.ini.html>`_


Suggestions
___________

* Use another interpolation style
* Use string concatenation
* Use a templating engine
* Use string replacement tool, such as str_replace()




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/DeprecateDollarCurly                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.1                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.2 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


