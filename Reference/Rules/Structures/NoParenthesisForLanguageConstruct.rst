.. _structures-noparenthesisforlanguageconstruct:

.. _no-parenthesis-for-language-construct:

No Parenthesis For Language Construct
+++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		No Parenthesis For Language Construct: Some PHP language constructs, such are ``include``, ``require``, ``include_once``, ``require_once``, ``print``, ``echo`` don't need parenthesis.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Parenthesis For Language Construct
	:twitter:description: No Parenthesis For Language Construct: Some PHP language constructs, such are ``include``, ``require``, ``include_once``, ``require_once``, ``print``, ``echo`` don't need parenthesis
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Parenthesis For Language Construct
	:og:type: article
	:og:description: Some PHP language constructs, such are ``include``, ``require``, ``include_once``, ``require_once``, ``print``, ``echo`` don't need parenthesis
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Parenthesis For Language Construct.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoParenthesisForLanguageConstruct.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoParenthesisForLanguageConstruct.html","name":"No Parenthesis For Language Construct","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Some PHP language constructs, such are ``include``, ``require``, ``include_once``, ``require_once``, ``print``, ``echo`` don't need parenthesis","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Parenthesis For Language Construct.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Some PHP language constructs, such are ``include``, ``require``, ``include_once``, ``require_once``, ``print``, ``echo`` don't need parenthesis. They accept parenthesis, but it is may lead to strange situations. 
It it better to avoid using parenthesis with ``echo``, ``print``, ``return``, ``throw``, ``yield``, ``yield from``, ``include``, ``require``, ``include_once``, ``require_once``.

.. code-block:: php
   
   <?php
   
   // This is an attempt to load 'foo.inc', or kill the script
   include('foo.inc') or die();
   // in fact, this is read by PHP as : include 1 
   // include  'foo.inc' or die();
   
   ?>

See also `ON PHP LANGUAGE CONSTRUCTS AND PARENTHESES <https://tfrommen.de/on-php-language-constructs-and-parentheses/>`_ and  `include <https://www.php.net/manual/en/function.include.php>`_.

Connex PHP features
-------------------

  + `parenthesis <https://php-dictionary.readthedocs.io/en/latest/dictionary/parenthesis.ini.html>`_
  + `language-construct <https://php-dictionary.readthedocs.io/en/latest/dictionary/language-construct.ini.html>`_
  + `return <https://php-dictionary.readthedocs.io/en/latest/dictionary/return.ini.html>`_
  + `include <https://php-dictionary.readthedocs.io/en/latest/dictionary/include.ini.html>`_


Suggestions
___________

* Remove parenthesis




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoParenthesisForLanguageConstruct                                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-parenthesis-for-language-construct <https://github.com/dseguy/clearPHP/tree/master/rules/no-parenthesis-for-language-construct.md>`__                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpdocumentor-structures-noparenthesisforlanguageconstruct`, :ref:`case-phpmyadmin-structures-noparenthesisforlanguageconstruct`                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


