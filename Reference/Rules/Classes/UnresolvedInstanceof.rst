.. _classes-unresolvedinstanceof:


.. _unresolved-instanceof:

Unresolved Instanceof
+++++++++++++++++++++


.. meta::

	:description:

		Unresolved Instanceof: The instanceof operator doesn't confirm if the compared class exists.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Unresolved Instanceof

	:twitter:description: Unresolved Instanceof: The instanceof operator doesn't confirm if the compared class exists

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Unresolved Instanceof

	:og:type: article

	:og:description: The instanceof operator doesn't confirm if the compared class exists

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unresolved Instanceof.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UnresolvedInstanceof.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UnresolvedInstanceof.html","name":"Unresolved Instanceof","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"The instanceof operator doesn't confirm if the compared class exists","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unresolved Instanceof.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The `instanceof <https://www.php.net/manual/en/language.operators.type.php>`_ operator doesn't confirm if the compared class exists. 

It checks if an variable is of a specific class. However, if the referenced class doesn't exist, because of a bug, a missed inclusion or a typo, the operator always fails, without a warning. 
Make sure the following classes are well defined.

.. code-block:: php
   
   <?php
   
   namespace X {
       class C {}
       
       // This is OK, as C is defined in X
       if ($o instanceof C) { }
   
       // This is not OK, as C is not defined in global
       // instanceof respects namespaces and use expressions
       if ($o instanceof \C) { }
   
       // This is not OK, as undefinedClass
       if ($o instanceof undefinedClass) { }
   
       // This is not OK, as $class is now a full namespace. It actually refers to \c, which doesn't exist
       $class = 'C';
       if ($o instanceof $class) { }
   }
   ?>

See also `Instanceof <https://www.php.net/manual/en/language.operators.type.php>`_.

Connex PHP features
-------------------

  + `instanceof <https://php-dictionary.readthedocs.io/en/latest/dictionary/instanceof.ini.html>`_


Suggestions
___________

* Remove the call to instanceof and all its dependencies.
* Fix the class name and use a class existing in the project.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnresolvedInstanceof                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-unresolved-instanceof <https://github.com/dseguy/clearPHP/tree/master/rules/no-unresolved-instanceof.md>`__                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-classes-unresolvedinstanceof`                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


