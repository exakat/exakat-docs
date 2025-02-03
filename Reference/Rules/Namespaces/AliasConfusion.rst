.. _namespaces-aliasconfusion:

.. _possible-alias-confusion:

Possible Alias Confusion
++++++++++++++++++++++++

.. meta::
	:description:
		Possible Alias Confusion: An alias is used for a class that doesn't belong to the current namespace, while there is such a class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Possible Alias Confusion
	:twitter:description: Possible Alias Confusion: An alias is used for a class that doesn't belong to the current namespace, while there is such a class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Possible Alias Confusion
	:og:type: article
	:og:description: An alias is used for a class that doesn't belong to the current namespace, while there is such a class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Possible Alias Confusion.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/AliasConfusion.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/AliasConfusion.html","name":"Possible Alias Confusion","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"An alias is used for a class that doesn't belong to the current namespace, while there is such a class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Possible Alias Confusion.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>An alias is used for a class that doesn't belong to the current namespace, while there is such a class. This also applies to traits and interfaces.

When no alias is used, PHP will search for a class in the local space. Since classes, traits and interfaces are usually stored one per file, it is a valid syntax to create an alias, even if this alias name is the name of a class in the same namespace. 

Yet, with an alias referring to a remote class, while a local one is available, it is possible to generate confusion.

.. code-block:: php
   
   <?php
   
   // This should be in a separate file, but has been merged here, for display purposes.
   namespace A {
       //an alias from a namespace called C
       use C\A as C_A;
   
       //an alias from a namespace called C, which will superseed the local A\B class (see below)
       use C\D as B;
   }
   
   namespace A {
       // There is a class B in the A namespace
       class B {}
   }
   
   ?>
Connex PHP features
-------------------

  + `semantics <https://php-dictionary.readthedocs.io/en/latest/dictionary/semantics.ini.html>`_


Suggestions
___________

* Avoid using existing classes names for alias
* Use a coding convention to distinguish alias from names




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/AliasConfusion                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+


