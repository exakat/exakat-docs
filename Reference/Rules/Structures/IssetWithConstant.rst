.. _structures-issetwithconstant:

.. _isset()-with-constants:

isset() With Constants
++++++++++++++++++++++

.. meta::
	:description:
		isset() With Constants: Until PHP 7, it was possible to use arrays as constants, but it was not possible to test them with isset.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: isset() With Constants
	:twitter:description: isset() With Constants: Until PHP 7, it was possible to use arrays as constants, but it was not possible to test them with isset
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: isset() With Constants
	:og:type: article
	:og:description: Until PHP 7, it was possible to use arrays as constants, but it was not possible to test them with isset
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/isset() With Constants.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/IssetWithConstant.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/IssetWithConstant.html","name":"isset() With Constants","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"Until PHP 7, it was possible to use arrays as constants, but it was not possible to test them with isset","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/isset() With Constants.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Until PHP 7, it was possible to use arrays as constants, but it was not possible to test them with `isset <https://www.www.php.net/isset>`_.

This would yield an `error <https://www.php.net/error>`_ : ``Cannot use `isset() <https://www.www.php.net/isset>`_ on the `result <https://www.php.net/result>`_ of an expression (you can use "null !== expression" instead)``. This is a backward incompatibility.

.. code-block:: php
   
   <?php
   const X = [1,2,3];
   
   if (isset(X[4])) {}
   ?>
Related PHP errors 
-------------------

  + `Cannot use isset() on the result of an expression (you can use "null !== expression" instead) <https://php-errors.readthedocs.io/en/latest/messages/cannot-use-isset%28%29-on-the-result-of-an-expression-%28you-can-use-%22null-%21%3D%3D-expression%22-instead%29.html>`_



Connex PHP features
-------------------

  + `isset <https://php-dictionary.readthedocs.io/en/latest/dictionary/isset.ini.html>`_


Suggestions
___________

* Avoid testing values on constants.




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/IssetWithConstant                                                                                                                                                                                                                                                                                 |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                                                                                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 7.0 and more recent                                                                                                                                                                                                                                                                                 |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                                                                                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Instant (5 mins)                                                                                                                                                                                                                                                                                             |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/issetWithConstant.html>`__                                                                                                                                                                                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                                                                                                                                    |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


