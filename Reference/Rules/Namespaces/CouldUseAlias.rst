.. _namespaces-couldusealias:

.. _could-use-alias:

Could Use Alias
+++++++++++++++

.. meta::
	:description:
		Could Use Alias: This long name may be reduced by using an available alias.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Use Alias
	:twitter:description: Could Use Alias: This long name may be reduced by using an available alias
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Use Alias
	:og:type: article
	:og:description: This long name may be reduced by using an available alias
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Use Alias.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/CouldUseAlias.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Namespaces\/CouldUseAlias.html","name":"Could Use Alias","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This long name may be reduced by using an available alias","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Use Alias.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This long name may be reduced by using an available alias.

This applies to classes (as full name or prefix), and to constants and functions.

.. code-block:: php
   
   <?php
   
   use a\b\c;
   use function a\b\c\foo;
   use const a\b\c\D;
   
   // This may be reduced with the above alias to c\d()
   new a\b\c\d();
   
   // This may be reduced to c\d\e\f 
   new a\b\c\d\e\f();
   
   // This may be reduced to c()
   new a\b\c();
   
   // This may be reduced to D
   echo a\b\c\D;
   
   // This may be reduced to D
   a\b\c\foo();
   
   // This can't be reduced : it is an absolute name
   \a\b\c\foo();
   
   // This can't be reduced : it is no an alias nor a prefix
   a\b\d\foo();
   
   ?>

See also `Using namespaces: Aliasing/Importing ¶ <https://www.php.net/manual/en/language.namespaces.importing.php>`_.

Connex PHP features
-------------------

  + `namespace <https://php-dictionary.readthedocs.io/en/latest/dictionary/namespace.ini.html>`_
  + `use-alias <https://php-dictionary.readthedocs.io/en/latest/dictionary/use-alias.ini.html>`_


Suggestions
___________

* Use all your aliases so as to make the code shorter and more readable
* Add new aliases for missing path
* Make class names absolute and drop the aliases




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/CouldUseAlias                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
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


