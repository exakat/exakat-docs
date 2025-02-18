.. _functions-nobooleanasdefault:


.. _no-boolean-as-default:

No Boolean As Default
+++++++++++++++++++++

.. meta::
	:description:
		No Boolean As Default: Default values should always be set up with a constant name.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Boolean As Default
	:twitter:description: No Boolean As Default: Default values should always be set up with a constant name
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Boolean As Default
	:og:type: article
	:og:description: Default values should always be set up with a constant name
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Boolean As Default.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NoBooleanAsDefault.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NoBooleanAsDefault.html","name":"No Boolean As Default","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 11 Feb 2025 09:13:38 +0000","dateModified":"Tue, 11 Feb 2025 09:13:38 +0000","description":"Default values should always be set up with a constant name","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Boolean As Default.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Default values should always be set up with a constant name.

Class constants and constants improve readability when calling the methods or comparing values and statuses.

.. code-block:: php
   
   <?php
   
   const CASE_INSENSITIVE = true;
   const CASE_SENSITIVE = false;
   
   function foo($case_insensitive = true) {
       // doSomething()
   }
   
   // Readable code 
   foo(CASE_INSENSITIVE);
   foo(CASE_SENSITIVE);
   
   // unreadable code  : is true case insensitive or case sensitive ? 
   foo(true);
   foo(false);
   
   ?>

See also `FlagArgument <https://www.martinfowler.com/bliki/FlagArgument.html>`_ and `Clean code: The curse of a boolean parameter <https://medium.com/@amlcurran/clean-code-the-curse-of-a-boolean-parameter-c237a830b7a3>`_.

Connex PHP features
-------------------

  + `Boolean <https://php-dictionary.readthedocs.io/en/latest/dictionary/boolean.ini.html>`_
  + `Default Value <https://php-dictionary.readthedocs.io/en/latest/dictionary/default-value.ini.html>`_


Suggestions
___________

* Use constants or class constants to give value to a boolean literal
* When constants have been defined, use them when calling the code
* Split the method into two methods, one for each case




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NoBooleanAsDefault                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.0                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openconf-functions-nobooleanasdefault`                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


