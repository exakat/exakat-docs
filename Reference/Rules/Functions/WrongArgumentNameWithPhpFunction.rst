.. _functions-wrongargumentnamewithphpfunction:


.. _wrong-argument-name-with-php-function:

Wrong Argument Name With PHP Function
+++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Wrong Argument Name With PHP Function: The name of the argument provided is not a valid parameter name for that PHP native function or method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong Argument Name With PHP Function
	:twitter:description: Wrong Argument Name With PHP Function: The name of the argument provided is not a valid parameter name for that PHP native function or method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong Argument Name With PHP Function
	:og:type: article
	:og:description: The name of the argument provided is not a valid parameter name for that PHP native function or method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Argument Name With PHP Function.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/WrongArgumentNameWithPhpFunction.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/WrongArgumentNameWithPhpFunction.html","name":"Wrong Argument Name With PHP Function","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The name of the argument provided is not a valid parameter name for that PHP native function or method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Wrong Argument Name With PHP Function.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The name of the argument provided is not a valid parameter name for that PHP native function or method. 
This analysis may be configured with extra PHP extensions or external packages.

.. code-block:: php
   
   <?php
   
   // those are the valid names
   strcmp(string1: 'a', string2: 'b');
   
   // those are not the valid names
   strcmp(string: 'a', stringToo: 'b');
   
   ?>

See also :ref:`Unknown Parameter Name <unknown-parameter-name>`.

Connex PHP features
-------------------

  + `Named Parameters <https://php-dictionary.readthedocs.io/en/latest/dictionary/named-parameter.ini.html>`_


Suggestions
___________

* Use the correct parameter name
* Remove all the parameter names from the call
* Create a relay function with the correct parameter names




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/WrongArgumentNameWithPhpFunction                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.3                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


