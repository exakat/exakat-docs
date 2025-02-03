.. _functions-unusedinheritedvariable:


.. _unused-inherited-variable-in-closure:

Unused Inherited Variable In Closure
++++++++++++++++++++++++++++++++++++


.. meta::

	:description:

		Unused Inherited Variable In Closure: Some closures forgot to make usage of inherited variables.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Unused Inherited Variable In Closure

	:twitter:description: Unused Inherited Variable In Closure: Some closures forgot to make usage of inherited variables

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Unused Inherited Variable In Closure

	:og:type: article

	:og:description: Some closures forgot to make usage of inherited variables

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unused Inherited Variable In Closure.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/UnusedInheritedVariable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/UnusedInheritedVariable.html","name":"Unused Inherited Variable In Closure","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Some closures forgot to make usage of inherited variables","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unused Inherited Variable In Closure.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Some closures forgot to make usage of inherited variables.

`Closure <https://www.php.net/manual/en/class.`closure <https://www.php.net/closure>`_.php>`_ have two separate set of incoming variables : the arguments (between parenthesis) and the inherited variables, in the 'use' clause. Inherited variables are extracted from the local environment at creation time, and keep their value until execution. 

The reported closures are requesting some local variables, but do not make any usage of them. They may be considered as dead code.

.. code-block:: php
   
   <?php
   
   // In this closure, $y is forgotten, but $u is used.
   $a = function ($y) use ($u) { return $u; };
   
   // In this closure, $u is forgotten
   $a = function ($y, $z) use ($u) { return $u; };
   
   ?>

See also `Anonymous functions <https://www.php.net/manual/en/functions.anonymous.php>`_.

Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_
  + `inherited-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/inherited-variable.ini.html>`_


Suggestions
___________

* Remove the unused inherited variable
* Make us of the unused inherited variable




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UnusedInheritedVariable                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.11                                                                                                                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-shopware-functions-unusedinheritedvariable`, :ref:`case-mautic-functions-unusedinheritedvariable`                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


