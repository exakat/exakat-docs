.. _php-nomorecurlyarrays:


.. _curly-bracketed-arrays-are-not-supported:

Curly-Bracketed Arrays Are Not Supported
++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Curly-Bracketed Arrays Are Not Supported: Only use square brackets to access array elements.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Curly-Bracketed Arrays Are Not Supported
	:twitter:description: Curly-Bracketed Arrays Are Not Supported: Only use square brackets to access array elements
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Curly-Bracketed Arrays Are Not Supported
	:og:type: article
	:og:description: Only use square brackets to access array elements
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Curly-Bracketed Arrays Are Not Supported.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NoMoreCurlyArrays.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NoMoreCurlyArrays.html","name":"Curly-Bracketed Arrays Are Not Supported","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Only use square brackets to access array elements","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Curly-Bracketed Arrays Are Not Supported.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Only use square brackets to access array elements. The usage of curly brackets for array access is deprecated since PHP 7.4.

.. code-block:: php
   
   <?php
   
   $array = [1,2,3];
   
   // always valid
   echo $array[1];
   
   // deprecated in PHP 7.4
   // removed in PHP 8.3
   echo $array{1};
   
   ?>

See also `Deprecate curly brace syntax <https://derickrethans.nl/phpinternalsnews-19.html>`_ and `Deprecate curly brace syntax for accessing array elements and string offsets <https://wiki.php.net/rfc/deprecate_curly_braces_array_access>`_.

Related PHP errors 
-------------------

  + `Array and string offset access syntax with curly braces is deprecated <https://php-errors.readthedocs.io/en/latest/messages/array-and-string-offset-access-syntax-with-curly-braces-is-deprecated.html>`_
  + `Array and string offset access syntax with curly braces is no longer supported <https://php-errors.readthedocs.io/en/latest/messages/array-and-string-offset-access-syntax-with-curly-braces-is-no-longer-supported.html>`_



Connex PHP features
-------------------

  + `Array With Curly Braces <https://php-dictionary.readthedocs.io/en/latest/dictionary/array-curly-braces.ini.html>`_


Suggestions
___________

* Always use square brackets to access particular index in an array




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NoMoreCurlyArrays                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


