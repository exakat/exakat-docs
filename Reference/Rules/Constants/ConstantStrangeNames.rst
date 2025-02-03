.. _constants-constantstrangenames:

.. _constants-with-strange-names:

Constants With Strange Names
++++++++++++++++++++++++++++

.. meta::
	:description:
		Constants With Strange Names: List of constants being defined with names that are incompatible with PHP standards.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Constants With Strange Names
	:twitter:description: Constants With Strange Names: List of constants being defined with names that are incompatible with PHP standards
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Constants With Strange Names
	:og:type: article
	:og:description: List of constants being defined with names that are incompatible with PHP standards
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Constants With Strange Names.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/ConstantStrangeNames.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/ConstantStrangeNames.html","name":"Constants With Strange Names","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"List of constants being defined with names that are incompatible with PHP standards","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Constants With Strange Names.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>List of constants being defined with names that are incompatible with PHP standards.

Constants names are valid when they satisfy the following regex : ``^[a-zA-Z_\x80-\xff][a-zA-Z0-9_\x80-\xff]*$``


.. code-block:: php
   
   <?php
   
   // Define a valid PHP constant
   define('ABC', 1); 
   const ABCD = 2; 
   
   // Define an invalid PHP constant
   define('ABC!', 1); 
   echo defined('ABC!') ? constant('ABC!') : 'Undefined';
   
   // Const doesn't allow illegal names
   
   ?>

See also `PHP Constants <https://www.php.net/manual/en/language.constants.php>`_.

Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Rename constants to be valid constants
* Adopt a naming conversion scheme, to translate names from an incompatible source to PHP's standard (and back).




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/ConstantStrangeNames                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Semantics <ruleset-Semantics>`                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


