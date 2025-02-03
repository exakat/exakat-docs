.. _complete-createmagicproperty:


.. _create-magic-property:

Create Magic Property
+++++++++++++++++++++

.. meta::
	:description:
		Create Magic Property: This command creates a link DEFINITION between a ``__get`` and ``__set`` calls, and its equivalent magic method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Create Magic Property
	:twitter:description: Create Magic Property: This command creates a link DEFINITION between a ``__get`` and ``__set`` calls, and its equivalent magic method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Create Magic Property
	:og:type: article
	:og:description: This command creates a link DEFINITION between a ``__get`` and ``__set`` calls, and its equivalent magic method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Create Magic Property.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/CreateMagicProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/CreateMagicProperty.html","name":"Create Magic Property","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This command creates a link DEFINITION between a ``__get`` and ``__set`` calls, and its equivalent magic method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Create Magic Property.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This command creates a link DEFINITION between a ``__get`` and ``__set`` calls, and its equivalent magic method.

It also adds links between ``__invoke`` and ``__toString`` in adapted situations.
This command may not detect all possible link for the ``__get`` and ``__set`` call. It may be missing information about the nature of the object.

.. code-block:: php
   
   <?php
   
   class x {
       function foo() {
           // This is linked to __set
           $this->a = 1;
           
           // This is linked to __get
           return $this->b;
       }
       
       function __get($name) {
           return 1;
       }
   
       function __set($name, $value) {
           // Store the value
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `magic-property <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-property.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/CreateMagicProperty                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


