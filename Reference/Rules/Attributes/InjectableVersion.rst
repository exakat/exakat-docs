.. _attributes-injectableversion:

.. _injectable-version:

Injectable Version
++++++++++++++++++

.. meta::
	:description:
		Injectable Version: The Injectable Version attribute mark a class in a class hierarchy to be the one to use when giving a type to a parameter, return type or property.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Injectable Version
	:twitter:description: Injectable Version: The Injectable Version attribute mark a class in a class hierarchy to be the one to use when giving a type to a parameter, return type or property
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Injectable Version
	:og:type: article
	:og:description: The Injectable Version attribute mark a class in a class hierarchy to be the one to use when giving a type to a parameter, return type or property
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Injectable Version.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/InjectableVersion.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/InjectableVersion.html","name":"Injectable Version","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"The Injectable Version attribute mark a class in a class hierarchy to be the one to use when giving a type to a parameter, return type or property","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Injectable Version.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The Injectable Version `attribute <https://www.php.net/attribute>`_ mark a class in a class hierarchy to be the one to use when giving a type to a parameter, return type or property.

For constructor, it is an implicit check. For other methods, the method has to be marked as ``CheckInjectableMethod`` to be checked. In case no `attribute <https://www.php.net/attribute>`_ is provided, both for ``InjectableVersion`` and ``CheckInjectableVersion``, no `error <https://www.php.net/error>`_ is returned.

The ``InjectableVersion`` allows to mark a specific class in a class hierarchy as the class to use in injections. 

The check applies to the whole method. 

The specifications include namespaces which are exempt from checking the `attribute <https://www.php.net/attribute>`_, namely test. This is not supported yet.

.. code-block:: php
   
   <?php
   
   #[InjectableVersion]
   abstract class Injectable {}
   
   class NotInjectable extends Injectable {}
   
   class x {
   	// CheckInjectableMethod is implicit for constructors
   	function __construct(Injectable $good, NotInjectable $wrong) {}
   
   	#[CheckInjectableVersion]
   	function good(Injectable $good, NotInjectable $wrong) {}
   }
   
   ?>

+------------------------+-------------------------+--------+-----------------------------------------------------------------------------------------+
| Name                   | Default                 | Type   | Description                                                                             |
+------------------------+-------------------------+--------+-----------------------------------------------------------------------------------------+
| injectableVersion      | \injectableversion      | string | The FQN for the InjectableVersion attribute. By default, it is in the global space      |
+------------------------+-------------------------+--------+-----------------------------------------------------------------------------------------+
| checkInjectableVersion | \checkinjectableversion | string | The FQN for the CheckInjectableVersion attribute. By default, it is in the global space |
+------------------------+-------------------------+--------+-----------------------------------------------------------------------------------------+



Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Attributes/InjectableVersion                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


