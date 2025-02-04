.. _php-scalararenotarrays:


.. _scalar-are-not-arrays:

Scalar Are Not Arrays
+++++++++++++++++++++

.. meta::
	:description:
		Scalar Are Not Arrays: It is wrong to use a scalar as an array, a warning is emitted.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Scalar Are Not Arrays
	:twitter:description: Scalar Are Not Arrays: It is wrong to use a scalar as an array, a warning is emitted
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Scalar Are Not Arrays
	:og:type: article
	:og:description: It is wrong to use a scalar as an array, a warning is emitted
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Scalar Are Not Arrays.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ScalarAreNotArrays.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ScalarAreNotArrays.html","name":"Scalar Are Not Arrays","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 14 Jan 2025 12:52:58 +0000","dateModified":"Tue, 14 Jan 2025 12:52:58 +0000","description":"It is wrong to use a scalar as an array, a warning is emitted","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Scalar Are Not Arrays.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

It is wrong to use a scalar as an array, a warning is emitted. PHP 7.4 emits a warning in such situations.

Typehinted argument with a scalar are reported by this analysis. Also, nullable arguments, both with typehint and return type hint.

.. code-block:: php
   
   <?php
   
   // Here, $x may be null, and in that case, the echo will fail.
   function foo(?A $x) { 
       echo $x[2]; 
   }
   
   ?>

See also `E_WARNING for invalid container read array-access <https://wiki.php.net/rfc/notice-for-non-valid-array-container>`_.

Related PHP errors 
-------------------

  + `Trying to access array offset on value of type null <https://php-errors.readthedocs.io/en/latest/messages/trying-to-access-array-offset-on-%25s.html>`_



Connex PHP features
-------------------

  + `Array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_
  + `ArrayObject <https://php-dictionary.readthedocs.io/en/latest/dictionary/arrayobject.ini.html>`_


Suggestions
___________

* Update type hints to avoid scalar values
* Remove the array syntax in the code using the results
* Cast to string type, so the array notation is accessible




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ScalarAreNotArrays                                                                                                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.0                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


