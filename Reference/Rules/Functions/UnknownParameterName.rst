.. _functions-unknownparametername:


.. _unknown-parameter-name:

Unknown Parameter Name
++++++++++++++++++++++

.. meta::
	:description:
		Unknown Parameter Name: The name of the parameter doesn't belong to the method signature.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unknown Parameter Name
	:twitter:description: Unknown Parameter Name: The name of the parameter doesn't belong to the method signature
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unknown Parameter Name
	:og:type: article
	:og:description: The name of the parameter doesn't belong to the method signature
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unknown Parameter Name.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/UnknownParameterName.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/UnknownParameterName.html","name":"Unknown Parameter Name","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"The name of the parameter doesn't belong to the method signature","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unknown Parameter Name.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The name of the parameter doesn't belong to the method signature. Named arguments were introduced in PHP 8.0.

Named arguments errors will also arise when spreading a hash array with arbitrary number of arguments. For example, with `array_merge() <https://www.php.net/array_merge>`_, the array should not use named keys.

.. code-block:: php
   
   <?php
   
   // All good
   foo(a:1, b:2, c:3);
   foo(...['a':1, 'b':2, 'c':3]);
   
   // A is not a parameter name, it should be a : names are case sensitive
   foo(A:1, b:2, c:3);
   foo(...['A':1, 'b':2, 'c':3]);
   
   function foo($a, $b, $c) {}
   
   array_merge(['a' => [1], 'b' => [2]]);
   ?>

See also `Named Arguments <https://wiki.php.net/rfc/named_params>`_ and :ref:`Wrong Argument Name With PHP Function <wrong-argument-name-with-php-function>`.

Related PHP errors 
-------------------

  + `Unknown named parameter $d in <https://php-errors.readthedocs.io/en/latest/messages/unknown-named-parameter-%24%25s.html>`_
  + `array_merge() does not accept unknown named parameters <https://php-errors.readthedocs.io/en/latest/messages/array_merge%28%29-does-not-accept-unknown-named-parameters.html>`_



Connex PHP features
-------------------

  + `Named Parameters <https://php-dictionary.readthedocs.io/en/latest/dictionary/named-parameter.ini.html>`_


Suggestions
___________

* Fix the name of the parameter and use a valid one
* Remove the parameter name, and revert to positional notation




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UnknownParameterName                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.6                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


