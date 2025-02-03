.. _complete-setclasspropertydefinitionwithtypehint:

.. _set-class-property-definition-with-type:

Set Class Property Definition With Type
+++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Set Class Property Definition With Type: Links method call to its definition, thanks to property typing.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Class Property Definition With Type
	:twitter:description: Set Class Property Definition With Type: Links method call to its definition, thanks to property typing
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Class Property Definition With Type
	:og:type: article
	:og:description: Links method call to its definition, thanks to property typing
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Set Class Property Definition With Type.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/SetClassPropertyDefinitionWithTypehint.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/SetClassPropertyDefinitionWithTypehint.html","name":"Set Class Property Definition With Type","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 24 Jan 2025 10:21:35 +0000","dateModified":"Fri, 24 Jan 2025 10:21:35 +0000","description":"Links method call to its definition, thanks to property typing","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Set Class Property Definition With Type.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Links method call to its definition, thanks to property typing. The link is ``DEFINITION``.

.. code-block:: php
   
   <?php
   
   class x {
       public x $p = null;
   
       public function bar() {
           return $this;
       }
   }
   
   $x = new x;
   
   // $x->p is of 'x' class
   $x->p->bar();
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetClassPropertyDefinitionWithTypehint                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


