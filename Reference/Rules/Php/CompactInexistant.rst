.. _php-compactinexistant:


.. _nonexistent-variable-in-compact():

Nonexistent Variable In compact()
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Nonexistent Variable In compact(): Compact() doesn't warn when it tries to work on an nonexistent variable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Nonexistent Variable In compact()
	:twitter:description: Nonexistent Variable In compact(): Compact() doesn't warn when it tries to work on an nonexistent variable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Nonexistent Variable In compact()
	:og:type: article
	:og:description: Compact() doesn't warn when it tries to work on an nonexistent variable
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Nonexistent Variable In compact().html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CompactInexistant.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/CompactInexistant.html","name":"Nonexistent Variable In compact()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"Compact() doesn't warn when it tries to work on an nonexistent variable","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Nonexistent Variable In compact().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`Compact() <https://www.php.net/compact>`_ doesn't warn when it tries to work on an nonexistent variable. It just ignores the variable.

This behavior changed in PHP 7.3, and `compact() <https://www.php.net/compact>`_ now emits a warning when the compacted variable doesn't exist.
For performances reasons, this analysis only works inside methods and functions.

.. code-block:: php
   
   <?php
   
   function foo($b = 2) {
       $a = 1;
       // $c doesn't exists, and is not compacted.
       return compact('a', 'b', 'c');
   }
   ?>

See also `compact <http://www.php.net/compact>`_ and `PHP RFC: Make compact function reports undefined passed variables <https://wiki.php.net/rfc/compact>`_.

Related PHP errors 
-------------------

  + `Undefined variable $a <https://php-errors.readthedocs.io/en/latest/messages/undefined-variable.html>`_



Connex PHP features
-------------------

  + `compact <https://php-dictionary.readthedocs.io/en/latest/dictionary/compact.ini.html>`_


Suggestions
___________

* Fix the name of variable in the compact() argument list
* Remove the name of variable in the compact() argument list




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CompactInexistant                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP73 <ruleset-CompatibilityPHP73>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.9                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


