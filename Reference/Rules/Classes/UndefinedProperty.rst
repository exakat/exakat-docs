.. _classes-undefinedproperty:


.. _undefined-properties:

Undefined Properties
++++++++++++++++++++

.. meta::
	:description:
		Undefined Properties: List of properties that are not explicitly defined in the class, its parents or traits.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Undefined Properties
	:twitter:description: Undefined Properties: List of properties that are not explicitly defined in the class, its parents or traits
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Undefined Properties
	:og:type: article
	:og:description: List of properties that are not explicitly defined in the class, its parents or traits
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Undefined Properties.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UndefinedProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UndefinedProperty.html","name":"Undefined Properties","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"List of properties that are not explicitly defined in the class, its parents or traits","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Undefined Properties.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

List of properties that are not explicitly defined in the class, its parents or traits.

It is possible to spot unidentified properties by using the PHP's magic methods ``__get`` and ``__set``. Even if the class doesn't use magic methods, any call to an undefined property will be directed to those methods, and they can be used as a canary, warning that the code is missing a definition. 

In PHP 8.2, undefined properties are reported as deprecated. They will become a Fatal `Error <https://www.php.net/error>`_ in PHP 9.0.

.. code-block:: php
   
   <?php
   
   class foo {
       // property definition
       private bar = 2;
       
       function foofoo() {
           // $this->bar is defined in the class
           // $this->barbar is NOT defined in the class
           return $this->bar + $this->barbar;
       }
   }
   
   ?>

See also `Properties <https://www.php.net/manual/en/language.oop5.properties.php>`_.

Related PHP errors 
-------------------

  + `Undefined property: %s::$%s <https://php-errors.readthedocs.io/en/latest/messages/undefined-property-%25s%3A%3A%24%25s.html>`_
  + `Property %s::$%s does not exist <https://php-errors.readthedocs.io/en/latest/messages/property-%25s-does-not-exist.html>`_



Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Suggestions
___________

* Add an explicit property definition, and give it ``null`` as a default value : this way, it behaves the same as undefined.
* Rename the property to one that exists already.




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Classes/UndefinedProperty                                                                                                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                                                                                                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.2 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/dynamicProperties.html>`__                                                                                                                          |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP         | `no-undefined-properties <https://github.com/dseguy/clearPHP/tree/master/rules/no-undefined-properties.md>`__                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples         | :ref:`case-wordpress-classes-undefinedproperty`, :ref:`case-mediawiki-classes-undefinedproperty`                                                                                                                                     |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule     | :ref:`checks-property-existence`                                                                                                                                                                                                     |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


