.. _interfaces-noconstructorininterface:

.. _no-constructor-in-interface:

No Constructor In Interface
+++++++++++++++++++++++++++

.. meta::
	:description:
		No Constructor In Interface: PHP manual recommends not adding constructors to interfaces.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Constructor In Interface
	:twitter:description: No Constructor In Interface: PHP manual recommends not adding constructors to interfaces
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Constructor In Interface
	:og:type: article
	:og:description: PHP manual recommends not adding constructors to interfaces
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Constructor In Interface.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/NoConstructorInInterface.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/NoConstructorInInterface.html","name":"No Constructor In Interface","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP manual recommends not adding constructors to interfaces","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Constructor In Interface.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>PHP manual recommends not adding constructors to interfaces. 

'Although they are supported, including constructors in interfaces is strongly discouraged. Doing so significantly reduces the flexibility of the object implementing the interface. Additionally, constructors are not enforced by inheritance rules, which can cause inconsistent and unexpected behavior.'

```

```

.. code-block:: php
   
   <?php
   
   interface with {
       function __construct();
   }
   
   ?>

See also `Object Interfaces <https://www.php.net/manual/en/language.oop5.interfaces.php>`_.

Connex PHP features
-------------------

  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Suggestions
___________

* Remove the constructor from the interface




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/NoConstructorInInterface                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.0                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


